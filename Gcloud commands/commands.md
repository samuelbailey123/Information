Notes for GCP Certification
Commands	What it does
Gcloud auth list	List active account name
gcloud config list project	List project ID
gcloud compute project-info describe --project <your_project_ID>	View project settings
gcloud container clusters create [CLUSTER-NAME]	Creates kubernetes cluster
gcloud container clusters get-credentials [CLUSTER-NAME]	Kubernetes credentials
kubectl create deployment hello-server --image=gcr.io/google-samples/hello-app:1.0	Deploy app into Kubernetes cluster
gcloud config set compute/zone us-central1-a	Set a default zone
gcloud config set compute/region us-central1	Set a default region
```gcloud compute instances create www3 \
  --image-family debian-9 \
  --image-project debian-cloud \
  --zone us-central1-a \
  --tags network-lb-tag \
  --metadata startup-script="#! /bin/bash
    sudo apt-get update
    sudo apt-get install apache2 -y
    sudo service apache2 restart
    echo '<!doctype html><html><body><h1>www3</h1></body></html>' | tee /var/www/html/index.html”```	Create a VM web server
```gcloud compute firewall-rules create www-firewall-network-lb \
    --target-tags network-lb-tag --allow tcp:80```	Create a firewall rule
```gcloud compute addresses create network-lb-ip-1 \
 --region us-central1```	Creat a load balancer
gcloud compute http-health-checks create basic-check	Add health check resource
```gcloud compute target-pools create www-pool \
    --region us-central1 --http-health-check basic-check```	Add target pool
```gcloud compute target-pools add-instances www-pool \
    --instances www1,www2,www3```	Add instances to target pool for LB
```gcloud compute forwarding-rules create www-rule \
    --region us-central1 \
    --ports 80 \
    --address network-lb-ip-1 \
    --target-pool www-pool```	Forwarding rule for LB to load pool
```gcloud compute instance-templates create lb-backend-template \
   --region=us-central1 \
   --network=default \
   --subnet=default \
   --tags=allow-health-check \
   --image-family=debian-9 \
   --image-project=debian-cloud \
   --metadata=startup-script='#! /bin/bash
     apt-get update
     apt-get install apache2 -y
     a2ensite default-ssl
     a2enmod ssl
     vm_hostname="$(curl -H "Metadata-Flavor:Google" \
     http://169.254.169.254/computeMetadata/v1/instance/name)"
     echo "Page served from: $vm_hostname" | \
     tee /var/www/html/index.html
     systemctl restart apache2’```	Create http LB
```gcloud compute instance-groups managed create lb-backend-group \
   --template=lb-backend-template --size=2 --zone=us-central1-a```	Create a managed instance group
```gcloud compute firewall-rules create fw-allow-health-check \
    --network=default \
    --action=allow \
    --direction=ingress \
    --source-ranges=130.211.0.0/22,35.191.0.0/16 \
    --target-tags=allow-health-check \
    --rules=tcp:80```	Create firewall rules
```gcloud compute addresses create lb-ipv4-1 \
    --ip-version=IPV4 \
    --global```	Global static IP
	
