## How to update Unifi Devices ##

- Copy the link location of the script.

- SSH into your Ubuntu/Debian machine, and login as root. ( Ubuntu | sudo -i | Debian | su )

- Make sure the ca-certificates package is installed.

apt-get update; apt-get install ca-certificates wget -y
- Download the script by executing the following command. ( change it to your wanted version )

```wget https://get.glennr.nl/unifi/install/unifi-5.13.32.sh```
Install the latest and greatest UniFi Network application with 1 line. ( copy paste )
```rm unifi-latest.sh &> /dev/null; wget https://get.glennr.nl/unifi/install/install_latest/unifi-latest.sh && bash unifi-latest.sh```
- Now run the script with the command below.

```bash unifi-5.13.32.sh```

##### Optional Parameters #####
The script has multiple options:
Option: --help
Shows script options and information.
Option: --skip
Skip any kind of manual input.
Option: --skip-install-haveged
Skip installation of haveged.
Option: --skip-swap
Skip swap file check/creation.
Option: --add-repository
Add UniFi Repository if --skip is used.
Option: --local-controller
Inform script that it's a local controller, to open port 10001/dup ( discovery ).
Option: --custom-url [argument]
Manually provide a UniFi Network application download URL. ( argument is optional )
example: --custom-url https://dl.ui.com/unifi/5.13.29/unifi_sysvinit_all.deb
Option: --v6
Run the Let's Encrypt script in IPv6 mode.
Option: --email [argument]
Specify what email address you want to use for Let's Encrypt renewal notifications.
example: --email glenn@glennr.nl
Option: --fqdn [argument]
Specify what domain name ( FQDN ) you want to use, you can specify multiple domain names with : as separator,.
Example: --fqdn glennr.nl:www.glennr.nl
Option: --server-ip [argument]
Specify the server IP address manually.
example: --server-ip 1.1.1.1
Option: --retry [argument]
Specify how many times the Let's Encrypt should retry the challenge/hostname resolving.
example: --retry 5
Option: --external-dns [argument] 
Use external DNS server to resolve the FQDN.
example: --external-dns 1.1.1.1
Option: --force-renew
Force renew the certificates.
Option: --dns-challenge
Runs the Let's Encrypt script in DNS mode instead of HTTP.
Option: --private-key [argument]
Specify path to your private key (paid certificate).
Example: --private-key /tmp/PRIVATE.key
Option: --signed-certificate [argument]
Specify path to your signed certificate (paid certificate).
example: --signed-certificate /tmp/SSL_CERTIFICATE.cer
Option: --chain-certificate [argument]
Specify path to your chain certificate (paid certificate).
example: --chain-certificate /tmp/CHAIN.cer
Option: --intermediate-certificate [argument]
Specify path to your intermediate certificate (paid certificate).
example: --intermediate-certificate /tmp/INTERMEDIATE.cer
Option: --own-certificate
Requirement if you want to import your own paid certificates with the use of --skip
 
##### Example command to run the script: #####
The example command installs the UniFi Network applicationwith Let's Encrypt certificates without any input from the user for glennr.nl and www.glennr.nl with email address glenn@glennr.nl for the renewal notifications.
bash unifi-5.13.29.sh --skip --fqdn glennr.nl:www.glennr.nl --email glenn@glennr.nl
- Once the installation is completed browse to your server IP address.

https://<ip-of-your-server>:8443
