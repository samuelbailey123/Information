# Overview

## Table of Contents

<table class="no-border">

<tbody>

<tr>

<td style="vertical-align: top;">

[1\. General Commands](#1)

[2\. VLANs](#2)

[3\. Port Operation](#3)

[4\. LAG (Link Aggregation)](#4)

[5\. SPAN (Port Mirroring)](#5)

[6\. Storm Control](#6)

[7\. Port Isolation (Protected Port)](#7)

[8\. Flow Control](#8)

[9\. QoS (Scheduling / Shaping / Policing)](#9)

</td>

<td style="vertical-align: top;">

[10\. Access-Lists (ACL)](#10) 

[11\. Spanning Tree (STP / RSTP)](#11)

[12\. MSTP](#12)

[13\. Port Error Disable / Auto Recovery](#13)

[14\. DHCP Guard / DHCP Snooping](#14)

[15\. ARP](#15)

[16\. DHCP Client / Static IP](#16)

[17\. IP Route (Static)](#17)

</td>

</tr>

</tbody>

</table>

<a name="1"></a>

## 1\. General Commands

<table style="width: 100%;">

<thead>

<tr class="fixed-table-head" style="background-color: #00a0df;">

<td class="wysiwyg-text-align-center" style="width: 102px;">

<font color="#ffffff">Description</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 266.031px;">

<font color="#ffffff"> USW-Leaf Command</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 290.969px;">

<font color="white">Cisco Command</font>

</td>

</tr>

</thead>

<tbody>

<tr>

<td style="width: 102px;">Show OS version information.</td>

<td class="wysiwyg-text-align-left" style="width: 266.031px;">UBNT# show version</td>

<td class="wysiwyg-text-align-left" style="width: 290.969px;">SW# show version</td>

</tr>

<tr>

<td style="width: 102px;">Show base MAC address.</td>

<td class="wysiwyg-text-align-left" style="width: 266.031px;">UBNT# show system</td>

<td class="wysiwyg-text-align-left" style="width: 290.969px;">SW# show version</td>

</tr>

<tr>

<td style="width: 102px;">Show USW Model.</td>

<td class="wysiwyg-text-align-left" style="width: 266.031px;">UBNT# show platform info</td>

<td class="wysiwyg-text-align-left" style="width: 290.969px;">SW# show version</td>

</tr>

<tr>

<td style="width: 102px;">Show current configuration (DRAM).</td>

<td class="wysiwyg-text-align-left" style="width: 266.031px;">UBNT# show running-config</td>

<td class="wysiwyg-text-align-left" style="width: 290.969px;">

<div>

<div>SW# show running-config</div>

</div>

</td>

</tr>

<tr>

<td style="width: 102px;">Show startup configuration (NVRAM).</td>

<td class="wysiwyg-text-align-left" style="width: 266.031px;">UBNT# show startup-config</td>

<td class="wysiwyg-text-align-left" style="width: 290.969px;">

<div>

<div>SW# show startup-config</div>

</div>

</td>

</tr>

<tr>

<td style="width: 102px;">Show all logs that the router has in its memory.</td>

<td class="wysiwyg-text-align-left" style="width: 266.031px;">UBNT# show log</td>

<td class="wysiwyg-text-align-left" style="width: 290.969px;">SW# show log</td>

</tr>

<tr>

<td style="width: 102px;">Overview all IPv4 interfaces on the switch.</td>

<td class="wysiwyg-text-align-left" style="width: 266.031px;">UBNT# show ip interface brief</td>

<td class="wysiwyg-text-align-left" style="width: 290.969px;">

<div>

<div>SW# show ip interface brief</div>

</div>

</td>

</tr>

<tr>

<td style="width: 102px;">Display current routing protocols.</td>

<td class="wysiwyg-text-align-left" style="width: 266.031px;">UBNT# show ip protocol</td>

<td class="wysiwyg-text-align-left" style="width: 290.969px;">

<div>

<div>SW# show ip protocol</div>

</div>

</td>

</tr>

<tr>

<td style="width: 102px;">Display IPv4 routing table.</td>

<td class="wysiwyg-text-align-left" style="width: 266.031px;">UBNT# show ip route</td>

<td class="wysiwyg-text-align-left" style="width: 290.969px;">SW# show ip route</td>

</tr>

<tr>

<td style="width: 102px;">Display IPv6 routing table.</td>

<td class="wysiwyg-text-align-left" style="width: 266.031px;">UBNT# show ipv6 route</td>

<td class="wysiwyg-text-align-left" style="width: 290.969px;">SW# show ipv6 route</td>

</tr>

<tr>

<td style="width: 102px;">Display access list.</td>

<td class="wysiwyg-text-align-left" style="width: 266.031px;">UBNT# show access-list <list_name></td>

<td class="wysiwyg-text-align-left" style="width: 290.969px;">

<div>

<div>SW# show access-list</div>

</div>

</td>

</tr>

<tr>

<td style="width: 102px;">Display MAC addresses table.</td>

<td class="wysiwyg-text-align-left" style="width: 266.031px;">UBNT# show platform mac address-table</td>

<td class="wysiwyg-text-align-left" style="width: 290.969px;">

<div>

<div>SW# show mac address-table</div>

</div>

</td>

</tr>

<tr>

<td style="width: 102px;">Show ARP table.</td>

<td class="wysiwyg-text-align-left" style="width: 266.031px;">UBNT# show arp</td>

<td class="wysiwyg-text-align-left" style="width: 290.969px;">SW# show arp</td>

</tr>

<tr>

<td style="width: 102px;">Display all users connected to the switch.</td>

<td class="wysiwyg-text-align-left" style="width: 266.031px;">N/A </td>

<td class="wysiwyg-text-align-left" style="width: 290.969px;">SW# show users</td>

</tr>

<tr>

<td style="width: 102px;">Display all info about flash memory.</td>

<td class="wysiwyg-text-align-left" style="width: 266.031px;">N/A</td>

<td class="wysiwyg-text-align-left" style="width: 290.969px;">SW# show flash</td>

</tr>

<tr>

<td style="width: 102px;">Display history of commands used.</td>

<td class="wysiwyg-text-align-left" style="width: 266.031px;">N/A</td>

<td class="wysiwyg-text-align-left" style="width: 290.969px;">SW# show history</td>

</tr>

<tr>

<td style="width: 102px;">Display the system clock.</td>

<td class="wysiwyg-text-align-left" style="width: 266.031px;">N/A </td>

<td class="wysiwyg-text-align-left" style="width: 290.969px;">SW# show clock</td>

</tr>

<tr>

<td style="width: 102px;">Information about hardware status.</td>

<td class="wysiwyg-text-align-left" style="width: 266.031px;">UBNT# show environment</td>

<td class="wysiwyg-text-align-left" style="width: 290.969px;">SW# show environment</td>

</tr>

<tr>

<td style="width: 102px;">Show the amount of switch free memory.</td>

<td class="wysiwyg-text-align-left" style="width: 266.031px;">UBNT# show memory</td>

<td class="wysiwyg-text-align-left" style="width: 290.969px;">SW# show memory</td>

</tr>

</tbody>

</table>

<a name="2"></a>

## 2\. VLANs

<table style="width: 100%;">

<thead>

<tr class="fixed-table-head" style="background-color: #00a0df;">

<td class="wysiwyg-text-align-center" style="width: 17px;">

<font color="#ffffff">Description</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 310.049px;">

<font color="#ffffff"> USW-Leaf Command</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 329.951px;">

<font color="white"> Cisco Command</font>

</td>

</tr>

</thead>

<tbody>

<tr>

<td style="width: 17px;">Display VLAN information, all ports which belong to specific VLAN, and information about the number of VLANs configured on the switch.</td>

<td style="width: 310.049px;">UBNT# show bridge-domain</td>

<td style="width: 329.951px;">SW# show vlan</td>

</tr>

<tr>

<td style="width: 17px;">Create new VLAN 2.</td>

<td style="width: 310.049px;">UBNT# configure terminal  
UBNT(config)# bridge-domain 2  
UBNT(bridge-domain)# exit  
UBNT(config)#</td>

<td style="width: 329.951px;">

<div>

<div>SW# configure terminal  
SW(config)# vlan 2  
SW(config-vlan)# exit</div>

</div>

</td>

</tr>

<tr>

<td id="" style="width: 17px;">

Add VLAN 2 membership to the port swp1, configure the native VLAN ID 10.

NPOS operates VLAN inside bridge-domain, so it's necessary to associate port with VLAN in bridge-domain.

</td>

<td style="width: 310.049px;">UBNT(config)# interface swp1  
UBNT(config-if)# switchport mode trunk  
UBNT(config-if)# switchport trunk allowed vlan 2  
UBNT(config-if)# switchport trunk native-vlan 10  
UBNT(config-if)# exit  
UBNT(config)# bridge-domain 2  
UBNT(bridge-domain)# vlan 2 swp1  
UBNT(bridge-domain)# exit  
UBNT(config)# bridge-domain 10  
UBNT(bridge-domain)# vlan 10 swp1  
UBNT(bridge-domain)# exit</td>

<td style="width: 329.951px;">

<div>

<div>SW(config)# interface fa1/0  
SW(config-if)# switchport mode trunk  
SW(config-if)# switchport trunk allowed vlan add 2  
SW(config-if)# switchport trunk native vlan 10  
SW(config-if)# exit</div>

</div>

</td>

</tr>

<tr>

<td style="width: 17px;">

Remove VLAN 2 membership from port swp1 and the native VLAN.

NPOS port with VLAN association to bridge-domain is removed automatically.

</td>

<td style="width: 310.049px;">UBNT(config)# interface swp1  
UBNT(config-if)# switchport trunk allowed vlan remove 2  
UBNT(config-if)# no switchport trunk native-vlan  
UBNT(config-if)# exit</td>

<td style="width: 329.951px;">

<div>

<div>SW(config)# interface fa1/0  
SW(config-if)# switchport trunk allowed vlan remove 2  
SW(config-if)# no switchport trunk native vlan  
SW(config-if)# exit</div>

</div>

</td>

</tr>

<tr>

<td style="width: 17px;">Enable or disable dot1q tagging for native VLANs on specific port. Cisco's method operates dot1q native tagging globally.</td>

<td style="width: 310.049px;">UBNT(config)# vlan do1q tag native  
UBNT(config)# interface swp1  
UBNT(config-if)# vlan dot1q tag native  
UBNT(config-if)# no vlan dot1q tag native  
UBNT(config-if)# exit</td>

<td style="width: 329.951px;">SW(config)# vlan do1q tag native  
SW(config)# no vlan do1q tag native</td>

</tr>

<tr>

<td style="width: 17px;">

Configure the swp1 interface as a nontrunking nontagged single-VLAN 3 access mode.

Before switching, disable the current mode.

</td>

<td style="width: 310.049px;">UBNT(config)# interface swp1  
UBNT(config-if)# no switchport  
UBNT(config-if)# switchport mode access  
UBNT(config-if)# switchport access vlan 3  
UBNT(config-if)# exit  
UBNT(config)# bridge-domain 3  
UBNT(bridge-domain)# vlan 3 swp1  
UBNT(bridge-domain)# exit</td>

<td style="width: 329.951px;">

<div>

<div>SW(config)# interface fa1/0  
SW(config-if)# switchport mode access  
SW(config-if)# switchport access vlan 3  
SW(config-if)# exit</div>

</div>

</td>

</tr>

<tr>

<td style="width: 17px;">Remove any configuration specific to Layer 2 on this interface (include VLAN's membership), switch interface to Layer 3 mode.</td>

<td style="width: 310.049px;">UBNT(config)# interface swp1  
UBNT(config-if)# no switchport  
UBNT(config-if)# exit</td>

<td style="width: 329.951px;">

<div>

<div>SW(config)# interface fa1/0  
SW(config-if)# no switchport  
SW(config-if)# exit</div>

</div>

</td>

</tr>

<tr>

<td style="width: 17px;">

Disable MAC address learning on a specified VLAN 2.

Maximum number of learning MAC records equal 1000.

Configure a secure sticky MAC address for interface swp1.

</td>

<td style="width: 310.049px;">UBNT(config)# bridge-domain 2  
UBNT(bridge-domain)# no learning enable  
UBNT(bridge-domain)# learning limit 1000  
UBNT(bridge-domain)# learning sticky aa:bb:cc:dd:11:22 interface swp1  
UBNT(bridge-domain)# exit</td>

<td style="width: 329.951px;">

<div>

<div>SW(config)# no mac-address-table learning vlan 2  
SW(config)# mac-address-table limit vlan 2 maximum 1000  
SW(config)# interface fa1/0  
SW(config-if)# switchport port-security mac-address aa:bb:cc:dd:11:22  
SW(config-if)# exit</div>

</div>

</td>

</tr>

</tbody>

</table>

<a name="3"></a>

## 3\. Port Operation

<table style="width: 100%;">

<thead>

<tr class="fixed-table-head" style="background-color: #00a0df;">

<td class="wysiwyg-text-align-center" style="width: 10px;">

<font color="#ffffff">Description</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 295.84px;">

<font color="#ffffff"> USW-Leaf Command</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 351.16px;">

<font color="white"> Cisco Command</font>

</td>

</tr>

</thead>

<tbody>

<tr>

<td style="width: 10px;">Show port status and admin state.</td>

<td style="width: 295.84px;">UBNT# show interface status</td>

<td style="width: 351.16px;">

<div>

<div>SW# show interface status</div>

</div>

</td>

</tr>

<tr>

<td style="width: 10px;">Verify the FEC feature status on the interface.</td>

<td style="width: 295.84px;">

<div>

<div>UBNT# show fec status</div>

</div>

</td>

<td style="width: 351.16px;"> </td>

</tr>

<tr>

<td style="width: 10px;">View the interface status of interface swp1.</td>

<td style="width: 295.84px;">UBNT# show port status swp1  
UBNT# show interface swp1</td>

<td style="width: 351.16px;">

<div>

<div>SW# show interface fa1/0</div>

</div>

</td>

</tr>

<tr>

<td style="width: 10px;">Display interface statistics.</td>

<td style="width: 295.84px;">UBNT# show statistics interface</td>

<td style="width: 351.16px;">

<div>

<div>SW# show interface counters</div>

</div>

</td>

</tr>

<tr>

<td style="width: 10px;">Clear interface statistics counters.</td>

<td style="width: 295.84px;">UBNT# show statistics clear</td>

<td style="width: 351.16px;">

<div>

<div>SW# clear counters</div>

</div>

</td>

</tr>

<tr>

<td style="width: 10px;">Display information about the connected transceivers.</td>

<td style="width: 295.84px;">UBNT# show interface transceiver swp1  
UBNT# show platform fwd interface sfp</td>

<td style="width: 351.16px;">

<div>

<div>SW# show interface transceiver</div>

</div>

</td>

</tr>

<tr>

<td style="width: 10px;">*Information about the switchport interface.</td>

<td style="width: 295.84px;">N/A</td>

<td style="width: 351.16px;">

<div>

<div>show interface switchport</div>

</div>

</td>

</tr>

<tr>

<td style="width: 10px;">Configure interface speed 100g, autonegotiation, and FEC cl-91.</td>

<td style="width: 295.84px;">UBNT(config)# interface swp54  
UBNT(config-if)# speed 100g  
UBNT(config-if)# autonegotiation enabled  
UBNT(config-if)# fec cl-91  
UBNT(config-if)# exit</td>

<td style="width: 351.16px;">

<div>

<div>SW(config)# interface fa1/0  
SW(config-if)# speed 100g  
SW(config-if)# speed auto  
SW(config-if)# fec cl91  
SW(config-if)# exit</div>

</div>

</td>

</tr>

<tr>

<td style="width: 10px;">Configure maximum transmission unit (MTU) size per specific interface.</td>

<td style="width: 295.84px;">UBNT(config)# interface swp54  
UBNT(config-if)# mtu 9216  
UBNT(config-if)# exit</td>

<td style="width: 351.16px;">

<div>

<div>SW(config)# interface fa1/0  
SW(config-if)# ip mtu 9216  
SW(config-if)# end</div>

</div>

</td>

</tr>

</tbody>

</table>

<a name="4"></a>

## 4\. LAG (Link Aggregation)

<table style="width: 100%;">

<thead>

<tr class="fixed-table-head" style="background-color: #00a0df;">

<td class="wysiwyg-text-align-center" style="width: 107px;">

<font color="#ffffff">Description</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 257.858px;">

<font color="#ffffff"> USW-Leaf Command</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 297.142px;">

<font color="white"> Cisco Command</font>

</td>

</tr>

</thead>

<tbody>

<tr>

<td style="width: 107px;">Display LACP internal information.</td>

<td style="width: 257.858px;">UBNT# show lacp internal</td>

<td style="width: 297.142px;">

<div>

<div>SW# show lacp internal</div>

</div>

</td>

</tr>

<tr>

<td style="width: 107px;">Display the status of a port-channel interface.</td>

<td style="width: 257.858px;">UBNT# show interface po1</td>

<td style="width: 297.142px;">

<div>

<div>SW# show interface port-channel 1</div>

</div>

</td>

</tr>

<tr>

<td style="width: 107px;">Display the traffic statistics for port channels.</td>

<td style="width: 257.858px;">UBNT# show lacp counters</td>

<td style="width: 297.142px;">

<div>

<div>SW# show lacp counters</div>

</div>

</td>

</tr>

<tr>

<td style="width: 107px;">Clear LACP counters.</td>

<td style="width: 257.858px;">UBNT# clear lacp counters</td>

<td style="width: 297.142px;">

<div>

<div>SW# clear lacp counters</div>

</div>

</td>

</tr>

<tr>

<td style="width: 107px;">Display the LACP system identifier.</td>

<td style="width: 257.858px;">UBNT# show lacp sys-id</td>

<td style="width: 297.142px;">

<div>

<div>SW# show lacp system-identifier</div>

</div>

</td>

</tr>

<tr>

<td style="width: 107px;">Display information about the LACP neighbor.</td>

<td style="width: 257.858px;">UBNT# show lacp neighbor</td>

<td style="width: 297.142px;">

<div>

<div>SW# show lacp neighbor</div>

</div>

</td>

</tr>

<tr>

<td style="width: 107px;">Configure the LACP system-priority and priority for the physical interface.</td>

<td style="width: 257.858px;">UBNT(config)# lacp system-priority 65535  
UBNT(config)# interface swp54  
UBNT(config-if)# lacp port-priority priority 20000  
UBNT(config-if)# exit</td>

<td style="width: 297.142px;">

<div>

<div>SW(config)# lacp system-priority 65535  
SW(config)# interface fa1/0  
SW(config-if)# lacp port-priority priority 20000  
SW(config-if)# exit</div>

</div>

</td>

</tr>

<tr>

<td style="width: 107px;">  

Specify the port mode as active for the links in a port channel.

Define the minimum and maximum number of active bundled.

Define LACP ports allowed in a port channel.

</td>

<td style="width: 257.858px;">UBNT(config)# interface swp1  
UBNT(config-if)# no switchport  
UBNT(config-if)# channel-group 1 mode active  
UBNT(config-if)# interface swp2  
UBNT(config-if)# no switchport  
UBNT(config-if)# channel-group 1 mode active  
UBNT(config-if)# interface port-channel 1  
UBNT(config-if)# lacp min-links 2  
UBNT(config-if)# lacp max-bundle 8  
UBNT(config-if)# exit</td>

<td style="width: 297.142px;">

<div>

<div>SW(config)# interface fa0/1  
SW(config-if)# channel-group 1 mode active  
SW(config-if)# interface fa0/2  
SW(config-if)# channel-group 1 mode active  
SW(config-if)# interface port-channel 1  
SW(config-if)# lacp min-links 2  
SW(config-if)# lacp max-bundle 8  
SW(config-if)# exit</div>

</div>

</td>

</tr>

<tr>

<td style="width: 107px;">Delete all interfaces from port-channel interface.</td>

<td style="width: 257.858px;">UBNT(config-if)# int po1  
UBNT(config-if)# delete all-lag-members  
UBNT(config-if)# exit</td>

<td style="width: 297.142px;">

<div>

<div>N/A</div>

</div>

</td>

</tr>

</tbody>

</table>

<a name="5"></a>

## 5\. SPAN (Port Mirroring)

<table style="width: 100%;">

<thead>

<tr class="fixed-table-head" style="background-color: #00a0df;">

<td class="wysiwyg-text-align-center" style="width: 108px;">

<font color="#ffffff">Description</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 257.326px;">

<font color="#ffffff"> USW-Leaf Command</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 296.674px;">

<font color="white"> Cisco Command</font>

</td>

</tr>

</thead>

<tbody>

<tr>

<td style="width: 108px;">Display information about the Switched Port Analyzer (SPAN).</td>

<td style="width: 257.326px;">UBNT# show mirror</td>

<td style="width: 296.674px;">

<div>

<div>SW# show monitor session</div>

</div>

</td>

</tr>

<tr>

<td style="width: 108px;">Set up a SPAN session (session 1) for monitoring ingress & egress port traffic to a destination port.</td>

<td style="width: 257.326px;">UBNT(config)# mirror tx session 1  
UBNT(config-mirror)# source interface swp1  
UBNT(config-mirror)# destination interface swp2  
UBNT(config)# mirror rx session 1  
UBNT(config-mirror)# source interface swp1  
UBNT(config-mirror)# destination interface swp2  
UBNT(config-mirror)# exit</td>

<td style="width: 296.674px;">

<div>

<div>SW(config)# monitor session 1 source interface fastEthernet0/1 tx  
SW(config)# monitor session 1 source interface fastEthernet0/1 rx  
SW(config)# monitor session 1 destination interface fastEthernet0/2</div>

</div>

</td>

</tr>

<tr>

<td style="width: 108px;">Delete SPAN sessions.</td>

<td style="width: 257.326px;">UBNT(config)# no mirror tx session 1  
UBNT(config)# no mirror rx session 1</td>

<td style="width: 296.674px;">

<div>

<div>SW(config)# no monitor session 1</div>

</div>

</td>

</tr>

</tbody>

</table>

<a name="6"></a>

## 6\. Storm Control

<table style="width: 100%;">

<thead>

<tr class="fixed-table-head" style="background-color: #00a0df;">

<td class="wysiwyg-text-align-center" style="width: 107px;">

<font color="#ffffff">Description</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 252.406px;">

<font color="#ffffff"> USW-Leaf Command</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 303.594px;">

<font color="white"> Cisco Command</font>

</td>

</tr>

</thead>

<tbody>

<tr>

<td style="width: 107px;">Display storm control statistics for specified interface.</td>

<td style="width: 252.406px;">UBNT# show statistics storm-control interface swp1</td>

<td style="width: 303.594px;">

<div>

<div>SW# show interface fa0/1 counters storm-control</div>

</div>

</td>

</tr>

<tr>

<td style="width: 107px;">Traffic Storm Control Configuration (level as a percentage of the total interface bandwidth).</td>

<td style="width: 252.406px;">UBNT(config)# interface swp1  
UBNT(config-if)# storm-control unicast level 50  
UBNT(config-if)# storm-control multicast level 50  
UBNT(config-if)# storm-control broadcast level 50  
UBNT(config-if)# exit</td>

<td style="width: 303.594px;">

<div>

<div>SW(config)# interface fa0/1  
SW(config-if)# storm-control unicast level 50  
SW(config-if)# storm-control multicast level 50  
SW(config-if)# storm-control broadcast level 50  
SW(config-if)# exit</div>

</div>

</td>

</tr>

</tbody>

</table>

<a name="7"></a>

## 7\. Port Isolation (Protected Port)

<table style="width: 100%;">

<thead>

<tr class="fixed-table-head" style="background-color: #00a0df;">

<td class="wysiwyg-text-align-center" style="width: 109px;">

<font color="#ffffff">Description</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 256.816px;">

<font color="#ffffff"> USW-Leaf Command</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 297.184px;">

<font color="white"> Cisco Command</font>

</td>

</tr>

</thead>

<tbody>

<tr>

<td style="width: 109px;">Display protected port state for specific interface.</td>

<td style="width: 256.816px;">UBNT# show interface swp1 switchport</td>

<td style="width: 297.184px;">

<div>

<div>SW# show interface fa0/1 switchport</div>

</div>

</td>

</tr>

<tr>

<td style="width: 109px;">Enable or disable the interface that will be a protected port.</td>

<td style="width: 256.816px;">UBNT(config)# interface swp1  
UBNT(config-if)# switchport protected  
UBNT(config-if)# no switchport protected  
UBNT(config-if)# exit</td>

<td style="width: 297.184px;">

<div>

<div>SW(config)# interface fa0/1  
SW(config-if)# switchport protected  
SW(config-if)# no switchport protected  
SW(config-if)# exit</div>

</div>

</td>

</tr>

</tbody>

</table>

<a name="8"></a>

## 8\. Flow Control<span class="wysiwyg-font-size-small"></span>

<table style="width: 100%;">

<thead>

<tr class="fixed-table-head" style="background-color: #00a0df;">

<td class="wysiwyg-text-align-center" style="width: 109px;">

<font color="#ffffff">Description</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 258.385px;">

<font color="#ffffff"> USW-Leaf Command</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 296.615px;">

<font color="white"> Cisco Command</font>

</td>

</tr>

</thead>

<tbody>

<tr>

<td style="width: 109px;">

<div>

<div>*Display the flow control settings.</div>

</div>

</td>

<td style="width: 258.385px;"> N/A</td>

<td style="width: 296.615px;">

<div>

<div>SW# show interface flowcontrol</div>

</div>

</td>

</tr>

<tr>

<td style="width: 109px;">

Configure flow-control mode

Configure flow-control priority

</td>

<td style="width: 258.385px;">UBNT(config)# interface swp1  
UBNT(config-if)# flow-control mode both  
UBNT(config-if)# priority-flow-control mode both  
UBNT(config-if)# exit</td>

<td style="width: 296.615px;">

<div>

<div>SW(config)# interface ethernet fa0/1  
SW(config-if)# flowcontrol receive on  
SW(config-if)# flowcontrol send on  
SW(config-if)#priority-flow-control mode on  
SW(config-if)# exit</div>

</div>

</td>

</tr>

<tr>

<td style="width: 109px;">Disable Link Level Flow Control and its priority on a specific interface.</td>

<td style="width: 258.385px;">UBNT(config)# interface swp1  
UBNT(config-if)# no flow-control  
UBNT(config-if)# no priority-flow-control  
UBNT(config-if)# exit</td>

<td style="width: 296.615px;">

<div>

<div>SW(config)# interface ethernet fa0/1  
SW(config-if)# flowcontrol receive off  
SW(config-if)# flowcontrol send off  
SW(config-if)#priority-flow-control mode off  
SW(config-if)# exit</div>

</div>

</td>

</tr>

</tbody>

</table>

<a name="9"></a>

## 9\. QoS (Scheduling / Shaping / Policing)<span class="wysiwyg-font-size-small"></span>

<table style="width: 100%;">

<thead>

<tr class="fixed-table-head" style="background-color: #00a0df;">

<td class="wysiwyg-text-align-center" style="width: 108px;">

<font color="#ffffff">Description</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 256.365px;">

<font color="#ffffff"> USW-Leaf Command</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 299.635px;">

<font color="white"> Cisco Command</font>

</td>

</tr>

</thead>

<tbody>

<tr>

<td style="width: 108px;">Verify existing scheduling policy, queues weight, and bound interfaces.</td>

<td style="width: 256.365px;">UBNT# show qos policy scheduling</td>

<td style="width: 299.635px;">SW# show mls qos interface queueing</td>

</tr>

<tr>

<td style="width: 108px;">Verify existing shaping policy.</td>

<td style="width: 256.365px;">UBNT# show qos policy shape</td>

<td style="width: 299.635px;" colspan="1" rowspan="2">

<div>SW# show policy-map interface</div>

</td>

</tr>

<tr>

<td style="width: 108px;">Verify existing policing policy.</td>

<td style="width: 256.365px;">UBNT# show qos policy policing</td>

</tr>

<tr>

<td style="width: 108px;">Configure the QoS Scheduling policy, binding the policy to a specific interface.</td>

<td style="width: 256.365px;">UBNT(config)# qos policy scheduling sch_pol  
UBNT(qos-policy)# queue 0 dwrr 5  
UBNT(qos-policy)# queue 1 dwrr 10  
UBNT(qos-policy)# queue 2 dwrr 20  
UBNT(qos-policy)# queue 3 dwrr 30  
UBNT(qos-policy)# queue 4 dwrr 40  
UBNT(qos-policy)# queue 5 dwrr 50  
UBNT(qos-policy)# queue 6 dwrr 60  
UBNT(qos-policy)# queue 7 dwrr 70  
UBNT(qos-policy)# exit  
UBNT(config)# interface swp1  
UBNT(config-if)# qos policy scheduling sch_pol  
UBNT(config-if)# exit</td>

<td style="width: 299.635px;">SW(config)# interface gigabitEthernet 1/0/1  
SW(config-if)# wrr-queue bandwidth 5 10 20 30 40 50 60 70  
SW(config-if)# exit</td>

</tr>

<tr>

<td style="width: 108px;">Configure the QoS Shaping policy, binding the policy to a specific interface.</td>

<td style="width: 256.365px;">UBNT(config)# qos policy shape shape_pol  
UBNT(qos-policy)# queue 0 min 2000 64000 max 10000 640000  
UBNT(qos-policy)# queue 1 min 2000 64000 max 20000 640000  
UBNT(qos-policy)# queue 2 min 2000 64000 max 20000 640000  
UBNT(qos-policy)# queue 3 min 2000 64000 max 30000 640000  
UBNT(qos-policy)# queue 4 min 2000 64000 max 40000 640000  
UBNT(qos-policy)# queue 5 min 2000 64000 max 50000 640000  
UBNT(qos-policy)# queue 6 min 2000 64000 max 60000 640000  
UBNT(qos-policy)# queue 7 min 2000 64000 max 70000 640000  
UBNT(qos-policy)# exit  
UBNT(config)# interface swp1  
UBNT(config-if)# qos policy shape shape_pol  
UBNT(config-if)# end</td>

<td class="" style="width: 299.635px;">SW(config)#policy-map shape_pol  
SW(config-pmap)#class shape_cl  
SW(config-pmap-c)#shape avarage 640000  
SWconfig-pmap-c)# exit  
SW(config)# interface gigabitEthernet 1/0/1  
SW(config-if)#service-policy output shape_pol  
SW(config-if)# exit</td>

</tr>

<tr>

<td style="width: 108px;">*Configure the QoS Policing policy that utilizes two ACLs (associated with policer), binding the policy to a specific interface.</td>

<td style="width: 256.365px;">UBNT(config)# ip access-list voice-acl  
UBNT(config-ip-acl)# 10 permit ip 192.168.10.0/24 any  
UBNT(config-ip-acl)# exit  
UBNT(config)# ip access-list database  
UBNT(config-ip-acl)# 10 permit tcp any any eq 1810  
UBNT(config-ip-acl)# 20 permit tcp any any eq 2481  
UBNT(config-ip-acl)# 30 permit tcp any any eq 1521  
UBNT(config-ip-acl)# exit  
UBNT(config)# policer aggregate voice-acl-aggr  
UBNT(qos-policer)# conform-action transmit  
UBNT(qos-policer)# exit  
UBNT(config)# policer aggregate database-aggr  
UBNT(qos-policer)# conform-action set-dscp 18  
UBNT(qos-policer)# exit  
UBNT(config)# qos policy policing test-policing  
UBNT(qos-policy-policing)# 10 access-list voice-acl  
UBNT(qos-policy-policing-acl)# policer voice-acl-aggr  
UBNT(qos-policy-policing-acl)# exit  
UBNT(qos-policy-policing)# 20 access-list database  
UBNT(qos-policy-policing-acl)# policer database-aggr  
UBNT(qos-policy-policing-acl)# exit  
UBNT(qos-policy-policing)# exit  
UBNT(config)# interface swp1  
UBNT(config-if)# qos policy policing test-policing input  
UBNT(config-if)# end</td>

<td class="" style="width: 299.635px;">SW(config)#ip access-list extended voice-acl  
SW(config-ext-nacl#permit ip 192.168.10.0 0.0.0.255 any  
SW(config-ext-nacl)#exit  
SW(config)#ip access-list extended database  
SW(config-ext-nacl)#permit tcp any any eq 1810  
SW(config-ext-nacl)#permit tcp any any eq 2481  
SW(config-ext-nacl)#permit tcp any any eq 1521  
SW(config-ext-nacl)#exit  
SW(config)#class-map class-voice  
SW(config-cmap)#match access-group name voice-acl  
SW(config-cmap)#exit  
SW(config)#class-map class-database  
SW(config-cmap)#match access-group name database  
SW(config-cmap)#exit  
SW(config)#policy-map test-policing  
SW(config-pmap)#class class-voice  
SW(config-pmap-c)#trust cos  
SW(config-pmap-c)#exit  
SW(config-pmap)#class class-database  
SW(config-pmap-c)#set dscp af21  
SW(config-pmap-c)#exit  
SW(config-pmap)#exit  
SW(config)#interface gigabitEthernet 1/0/1  
SW(config-if)#service-policy input test-policing  
SW(config-if)#exit</td>

</tr>

<tr>

<td style="width: 108px;">Unbind the scheduling, shaping and policing policies from a specific interface.</td>

<td style="width: 256.365px;">UBNT(config)# interface swp1  
UBNT(config-if)# no qos policy scheduling  
UBNT(config-if)# no qos policy shape  
UBNT(config-if)# no qos policy policing input  
UBNT(config-if)# exit</td>

<td style="width: 299.635px;">SW(config)# interface gigabitEthernet 1/0/1  
SW(config-if)# no wrr-queue bandwidth  
SW(config-if)# no service-policy output shape_pol  
SW(config-if)# no service-policy input test-policing  
SW(config-if)# exit</td>

</tr>

</tbody>

</table>

<a name="10"></a>

## 10\. Access-Lists (ACL)

<table style="width: 100%;">

<thead>

<tr class="fixed-table-head" style="background-color: #00a0df;">

<td class="wysiwyg-text-align-center" style="width: 107px;">

<font color="#ffffff">Description</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 255.177px;">

<font color="#ffffff"> USW-Leaf Command</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 301.823px;">

<font color="white"> Cisco Command</font>

</td>

</tr>

</thead>

<tbody>

<tr>

<td style="width: 107px;">Show the MAC access list configuration.</td>

<td style="width: 255.177px;">UBNT# show access-lists mac-acl</td>

<td style="width: 301.823px;">SW# show mac access-lists mac-acl</td>

</tr>

<tr>

<td style="width: 107px;">Show the IP access list configuration.</td>

<td style="width: 255.177px;">UBNT# show access-lists ip-acl</td>

<td style="width: 301.823px;">SW# show ip access-lists ip-acl</td>

</tr>

<tr>

<td style="width: 107px;">*MAC ACL Configuration</td>

<td style="width: 255.177px;">UBNT(config)# mac access-list mac-acl  
UBNT(config-mac-acl)# 10 permit any 0000.aaaa.0001 ffff.ffff.ffff any  
UBNT(config-mac-acl)# 20 permit any 0000.aaaa.0002 ffff.ffff.ffff any  
UBNT(config-mac-acl)# no sequence 20  
UBNT(config-mac-acl)# exit</td>

<td style="width: 301.823px;">SW(config)#mac access-list extended mac-acl  
SW(config-ext-macl)#permit any host 0000.aaaa.0001  
SW(config-ext-macl)#permit any host 0000.aaaa.0002  
SW(config-ext-macl)#no permit any host 0000.aaaa.0002  
SW(config-ext-macl)#exit</td>

</tr>

<tr>

<td style="width: 107px;">IP ACL Configuration</td>

<td style="width: 255.177px;">SW(config)# ip access-list ip-acl  
SW(config-ip-acl)# 10 permit ip 192.168.10.0/24 any  
SW(config-ip-acl)# 20 deny tcp any any eq 8080  
SW(config-ip-acl)# exit</td>

<td style="width: 301.823px;">SW(config)#ip access-list extended ip-acl  
SW(config-ext-ipacl)#permit ip 192.168.10.0 0.0.0.255 any  
SW(config-ext-ipacl)#deny tcp any any eq 8080  
SW(config-ext-ipacl)#exit</td>

</tr>

<tr>

<td style="width: 107px;">Apply MAC ACL and IP ACL to the specific interface.</td>

<td style="width: 255.177px;">UBNT(config-mac-acl)# interface swp1  
UBNT(config-if)# mac access-group mac-acl in  
UBNT(config-if)# ip access-group ip-acl in  
UBNT(config-mac-acl)# exit</td>

<td style="width: 301.823px;">SW(config)# interface gigabitEthernet 1/0/1  
SW(config-if)# mac access-group mac-acl in  
SW(config-if)# ip access-group ip-acl in  
SW(config-if)# exit</td>

</tr>

<tr>

<td style="width: 107px;">Remove MAC ACL and IP ACL from the specific interface.</td>

<td style="width: 255.177px;">UBNT(config-mac-acl)# interface swp1  
UBNT(config-if)# no mac access-group in  
UBNT(config-if)# no ip access-group in  
UBNT(config-mac-acl)# exit</td>

<td style="width: 301.823px;">SW(config)# interface gigabitEthernet 1/0/1  
SW(config-if)# no mac access-group mac-acl in  
SW(config-if)# no ip access-group ip-acl in  
SW(config-if)# exit</td>

</tr>

</tbody>

</table>

<a name="11"></a>

## 11\. Spanning Tree (STP / RSTP)

<table style="width: 100%;">

<thead>

<tr class="fixed-table-head" style="background-color: #00a0df;">

<td class="wysiwyg-text-align-center" style="width: 109px;">

<font color="#ffffff">Description</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 253.76px;">

<font color="#ffffff"> USW-Leaf Command</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 300.24px;">

<font color="white"> Cisco Command</font>

</td>

</tr>

</thead>

<tbody>

<tr>

<td style="width: 109px;">Display Spanning Tree information.</td>

<td style="width: 253.76px;">UBNT# show spanning-tree stp</td>

<td style="width: 300.24px;">SW# show spanning-tree</td>

</tr>

<tr>

<td style="width: 109px;">Display a brief summary about STP.</td>

<td style="width: 253.76px;">UBNT# show spanning-tree interface brief</td>

<td style="width: 300.24px;">SW# show spanning-tree brief</td>

</tr>

<tr>

<td style="width: 109px;">Display the STP interface status and configuration of specified interface.</td>

<td style="width: 253.76px;">UBNT# show spanning-tree interface swp1</td>

<td style="width: 300.24px;">SW# show spanning-tree interface gigabitEthernet 1/0/1</td>

</tr>

<tr>

<td style="width: 109px;">Display Rapid Spanning Tree information.</td>

<td style="width: 253.76px;">UBNT# show spanning-tree rstp</td>

<td style="width: 300.24px;">SW# show spanning-tree</td>

</tr>

<tr>

<td style="width: 109px;">Configure Spanning Tree Properties.</td>

<td style="width: 253.76px;">UBNT(config)# spanning-tree  
UBNT(config)# spanning-tree mode stp  
UBNT(config)# spanning-tree priority 32768  
UBNT(config)# spanning-tree forward-time 15  
UBNT(config)# spanning-tree max-age 20  
UBNT(config)# spanning-tree hello-time 2  
UBNT(config)# spanning-tree transmit hold-count 4  
UBNT(config)# spanning-tree pathcost-method long  
UBNT(config)# exit</td>

<td style="width: 300.24px;">SW(config)# spanning-tree  
SW(config)# spanning-tree mode stp  
SW(config)# spanning-tree priority 32768  
SW(config)# spanning-tree forward-time 15  
SW(config)# spanning-tree max-age 20  
SW(config)# spanning-tree hello-time 2  
SW(config)# spanning-tree transmit hold-count 4  
SW(config)# spanning-tree pathcost-method long  
SW(config)# exit</td>

</tr>

<tr>

<td style="width: 109px;">Specify that the Rapid STP is enabled.</td>

<td style="width: 253.76px;">UBNT(config)# spanning-tree mode rstp</td>

<td style="width: 300.24px;">SW(config)# spanning-tree mode rstp</td>

</tr>

<tr>

<td style="width: 109px;">Disable Spanning Tree globally.</td>

<td style="width: 253.76px;">UBNT(config)# no spanning-tree</td>

<td style="width: 300.24px;">SW(config)#no spanning-tree</td>

</tr>

<tr>

<td style="width: 109px;">*Enable or disable BPDU Guard for an interface.</td>

<td style="width: 253.76px;">UBNT(config)# interface swp1.1  
UBNT(config-if)# spanning-tree bpdu-guard  
UBNT(config-if)# no spanning-tree bpdu-guard</td>

<td style="width: 300.24px;">SW(config)# interface gigabitEthernet 1/0/1  
SW(config-if)# spanning-tree bpduguard enable  
SW(config-if)# spanning-tree bpduguard disable</td>

</tr>

<tr>

<td style="width: 109px;">*Enable or disable Loop Guard for an interface.</td>

<td style="width: 253.76px;">UBNT(config)# interface swp1.1  
UBNT(config-if)# spanning-tree loopback-detection  
UBNT(config-if)# no spanning-tree loopback-detection</td>

<td style="width: 300.24px;">SW(config)# interface gigabitEthernet 1/0/1  
SW(config-if)# spanning-tree loopguard default  
SW(config-if)# no spanning-tree loopguard default</td>

</tr>

<tr>

<td style="width: 109px;">*Enable or disable Root Guard for an interface.</td>

<td style="width: 253.76px;">UBNT(config)# interface swp1.1  
UBNT(config-if)# spanning-tree root-guard  
UBNT(config-if)# no spanning-tree root-guard</td>

<td style="width: 300.24px;">SW(config)# interface gigabitEthernet 1/0/1  
SW(config-if)# spanning-tree guard root  
SW(config-if)# no spanning-tree guard root</td>

</tr>

</tbody>

</table>

<a name="12"></a>

## 12\. MSTP

<table style="width: 100%;">

<thead>

<tr class="fixed-table-head" style="background-color: #00a0df;">

<td class="wysiwyg-text-align-center" style="width: 109px;">

<font color="#ffffff">Description</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 248.965px;">

<font color="#ffffff"> USW-Leaf Command</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 305.035px;">

<font color="white"> Cisco Command</font>

</td>

</tr>

</thead>

<tbody>

<tr>

<td style="width: 109px;">Display Multiple Spanning Tree configuration information.</td>

<td style="width: 248.965px;">UBNT# show spanning-tree mst configuration</td>

<td style="width: 305.035px;">SW# show spanning-tree mst configuration</td>

</tr>

<tr>

<td style="width: 109px;">Display Multiple Spanning Tree specific instance information.</td>

<td style="width: 248.965px;">UBNT# show spanning-tree mst 1 status</td>

<td style="width: 305.035px;">SW# show spanning-tree mst 1</td>

</tr>

<tr>

<td style="width: 109px;">Displays a brief summary about specific MSTP instance.</td>

<td style="width: 248.965px;">UBNT# show spanning-tree mst 1 interface brief</td>

<td style="width: 305.035px;"> </td>

</tr>

<tr>

<td style="width: 109px;">Configure Multiple Spanning Tree Properties.</td>

<td style="width: 248.965px;">UBNT(config)# spanning-tree mode mst  
UBNT(config)# spanning-tree mst max-hops 22  
UBNT(config)# spanning-tree mst name test_inst  
UBNT(config)# spanning-tree mst revision 32768</td>

<td style="width: 305.035px;">SW(config)# spanning-tree mode mst  
SW(config)# spanning-tree mst max-hops 22  
SW(config)# spanning-tree mst configuration  
SW(config-mst)# name test_inst  
SW(config-mst)# revision 32768  
SW(config-mst)# exit</td>

</tr>

<tr>

<td style="width: 109px;">Configure instance priority, and add VLAN 100 to MST instance 2.</td>

<td style="width: 248.965px;">UBNT(config)# spanning-tree mst 2 priority 61440  
UBNT(config)# spanning-tree instance 2 domain 100</td>

<td style="width: 305.035px;">SW(config)# spanning-tree mst 2 priority 61440  
SW(config)# spanning-tree mst configuration  
SW(config-mst)# instance 2 vlan 100  
SW(config-mst)# exit</td>

</tr>

<tr>

<td style="width: 109px;">*STP/MSTP interface related commands for special interface(swp1) in specific vlan(100).</td>

<td style="width: 248.965px;">UBNT(config-if)# interface swp1.100  
UBNT(config-if)# spanning-tree link-type point-to-point  
UBNT(config-if)# spanning-tree cost 10000  
UBNT(config-if)# spanning-tree port-priority 32  
UBNT(config-if)# spanning-tree edge-port</td>

<td style="width: 305.035px;">SW(config)# interface gigabitEthernet 1/0/1  
SW(config-if)# spanning-tree link-type point-to-point  
SW(config-if)# spanning-tree mst <instance-id> port-priority 32  
SW(config-if)# spanning-tree mst <instance-id> cost 10000  
SW(config-if)# spanning-tree portfast</td>

</tr>

</tbody>

</table>

<a name="13"></a>

## 13\. Port Error Disable / Auto Recovery

<table style="width: 100%;">

<thead>

<tr class="fixed-table-head" style="background-color: #00a0df;">

<td class="wysiwyg-text-align-center" style="width: 115px;">

<font color="#ffffff">Description</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 245.458px;">

<font color="#ffffff"> USW-Leaf Command</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 302.542px;">

<font color="white"> Cisco Command</font>

</td>

</tr>

</thead>

<tbody>

<tr>

<td style="width: 115px;">Display the time period after which the interfaces are enabled for 'errdisable' conditions.</td>

<td style="width: 245.458px;">UBNT# show errdisable recovery</td>

<td style="width: 302.542px;">SW# show errdisable recovery</td>

</tr>

<tr>

<td style="width: 115px;">Display the reason for the 'errdisable' status.</td>

<td style="width: 245.458px;">UBNT# show errdisable detect</td>

<td style="width: 302.542px;">SW# show errdisable detect</td>

</tr>

<tr>

<td style="width: 115px;">Configure 'errdisable' recovery interval.</td>

<td style="width: 245.458px;">UBNT(config)# errdisable recovery interval 400</td>

<td style="width: 302.542px;">SW(config)# errdisable recovery interval 400</td>

</tr>

<tr>

<td style="width: 115px;">*Enable or disable the BPDU guard 'errdisable' recovery condition.</td>

<td style="width: 245.458px;">UBNT(config)# errdisable recovery cause bpduguard  
UBNT(config)# no errdisable recovery cause bpduguard</td>

<td style="width: 302.542px;">SW(config)# errdisable recovery cause bpduguard  
SW(config)# no errdisable recovery cause bpduguard</td>

</tr>

</tbody>

</table>

<a name="14"></a>

## 14\. DHCP Guard / DHCP Snooping

<table style="width: 100%;">

<thead>

<tr class="fixed-table-head" style="background-color: #00a0df;">

<td class="wysiwyg-text-align-center" style="width: 112px;">

<font color="#ffffff">Description</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 247.538px;">

<font color="#ffffff"> USW-Leaf Command</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 302.462px;">

<font color="white"> Cisco Command</font>

</td>

</tr>

</thead>

<tbody>

<tr>

<td style="width: 112px;">Display DHCP guard settings.</td>

<td style="width: 247.538px;">UBNT# show ip dhcp guard</td>

<td style="width: 302.462px;">SW# show ip dhcp snooping binding</td>

</tr>

<tr>

<td style="width: 112px;">Enable or disable DHCP Guard.</td>

<td style="width: 247.538px;">UBNT(config)# ip dhcp guard  
UBNT(config)# no ip dhcp guard</td>

<td style="width: 302.462px;">SW(config)# ip dhcp snooping  
SW(config)# no ip dhcp snooping</td>

</tr>

<tr>

<td style="width: 112px;">Add or remove trusted DHCP server to special VLAN (Cisco uses the trust interface approach).</td>

<td style="width: 247.538px;">UBNT(config)# ip dhcp guard vlan 23 server 172.16.1.1  
UBNT(config)# no ip dhcp guard vlan 23 server 172.16.1.1</td>

<td style="width: 302.462px;">SW(config)# ip dhcp snooping vlan 23  
SW(config)# interface gigabitEthernet 1/0/1  
SW(config-if)# ip dhcp snooping trust  
SW(config-if)# no ip dhcp snooping trust</td>

</tr>

</tbody>

</table>

<a name="15"></a>

## 15\. ARP<span class="wysiwyg-font-size-small"></span>

<table style="width: 100%;">

<thead>

<tr class="fixed-table-head" style="background-color: #00a0df;">

<td class="wysiwyg-text-align-center" style="width: 108px;">

<font color="#ffffff">Description</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 252.007px;">

<font color="#ffffff"> USW-Leaf Command</font>

</td>

<td class="wysiwyg-text-align-left" style="width: 302.993px;">

<font color="white"> Cisco Command</font>

</td>

</tr>

</thead>

<tbody>

<tr>

<td style="width: 108px;">Display ARP table.</td>

<td style="width: 252.007px;">UBNT# show arp</td>

<td style="width: 302.993px;">SW# show ip arp</td>

</tr>

<tr>

<td style="width: 108px;">Configure ARP aging time globally and per specific interface.</td>

<td style="width: 252.007px;">UBNT(config)# arp aging-time 300  
UBNT(config)# int swp1  
UBNT(config-if)# arp aging-time 3600  
UBNT(config-if)# exit</td>

<td style="width: 302.993px;">SW(config)# arp timeout 300  
SW(config)# interface gigabitEthernet 1/0/1  
SW(config-if)# arp timeout 3600  
SW(config-if)# exit</td>

</tr>

<tr>

<td style="width: 108px;">Add or remove static ARP entry.</td>

<td style="width: 252.007px;">UBNT(config)# ip arp 10.1.1.1 44:d9:e7:9e:b6:db port swp1  
UBNT(config)# no ip arp 10.1.1.1 44:d9:e7:9e:b6:db</td>

<td style="width: 302.993px;">SW(config)# interface gigabitEthernet 1/0/1  
SW(config-if)# ip arp 10.1.1.1 44:d9:e7:9e:b6:db  
SW(config-if)# no ip arp 10.1.1.1 44:d9:e7:9e:b6:db</td>

</tr>

<tr>

<td style="width: 108px;">Clear the ARP table.</td>

<td style="width: 252.007px;">UBNT# clear arp all</td>

<td style="width: 302.993px;">SW# clear ip arp</td>

</tr>

</tbody>

</table>

<a name="16"></a>

## 16\. DHCP Client / Static IP

<table style="width: 100%;">

<thead>

<tr class="fixed-table-head" style="background-color: #00a0df;">

<td class="wysiwyg-text-align-center" style="width: 106px;">

<font color="#ffffff">Description</font>

</td>

<td class="wysiwyg-text-align-center" style="width: 248.524px;">

<font color="#ffffff"> USW-Leaf Command</font>

</td>

<td class="wysiwyg-text-align-center" style="width: 308.476px;">

<font color="white"> Cisco Command</font>

</td>

</tr>

</thead>

<tbody>

<tr>

<td style="width: 106px;">Overview all IPv4 interfaces on the switch.</td>

<td style="width: 248.524px;">UBNT# show ip interface brief</td>

<td style="width: 308.476px;">SW# show ip interface brief</td>

</tr>

<tr>

<td style="width: 106px;">Enable/Disable DHCP Client on bridge-domain interface.</td>

<td style="width: 248.524px;">UBNT(config)# interface bridge 1  
UBNT(config-if)# ip address dhcp  
UBNT(config-if)# no ip address dhcp  
UBNT(config-if)# exit</td>

<td style="width: 308.476px;">SW(config)# interface vlan1  
SW(config-if)# ip address dhcp  
SW(config-if)# no ip address dhcp  
SW(config-if)# exit</td>

</tr>

<tr>

<td style="width: 106px;">Configure/Remove static IP address on interface.</td>

<td style="width: 248.524px;">UBNT(config)# interface swp1  
UBNT(config-if)# ip address 172.16.0.1/24  
UBNT(config-if)# no ip address 172.16.0.1/24  
UBNT(config-if)# exit</td>

<td style="width: 308.476px;">SW(config)# interface gigabitEthernet 1/0/1  
SW(config-if)# ip address 172.16.0.1 255.255.255.0  
SW(config-if)# no ip address 172.16.0.1  
SW(config-if)# exit</td>

</tr>

</tbody>

</table>

<a name="17"></a>

## 17\. IP Route (Static)<span class="wysiwyg-font-size-small"></span>

<table style="width: 100%;">

<thead>

<tr class="fixed-table-head" style="background-color: #00a0df;">

<td class="wysiwyg-text-align-center" style="width: 134px;">

<font color="#ffffff">Description</font>

</td>

<td class="wysiwyg-text-align-center" style="width: 231.233px;">

<font color="#ffffff"> USW-Leaf Command</font>

</td>

<td class="wysiwyg-text-align-center" style="width: 297.767px;">

<font color="white"> Cisco Command</font>

</td>

</tr>

</thead>

<tbody>

<tr>

<td style="width: 134px;">Display IPv4 routing table.</td>

<td style="width: 231.233px;">UBNT# sh ip route</td>

<td style="width: 297.767px;">SW# show ip route</td>

</tr>

<tr>

<td style="width: 134px;">Configure/Remove default static route.</td>

<td style="width: 231.233px;">UBNT(config)# ip route 0.0.0.0/0 192.168.1.1  
UBNT(config)# no ip route 0.0.0.0/0 192.168.1.1</td>

<td style="width: 297.767px;">SW(config)# ip route 0.0.0.0 0.0.0.0 192.168.1.1  
SW(config)# no ip route 0.0.0.0 0.0.0.0 192.168.1.1</td>

</tr>

<tr>

<td style="width: 134px;">Configure/Remove static route to specific network.</td>

<td style="width: 231.233px;">UBNT(config)# ip route 172.16.1.0/24 192.168.1.1  
UBNT(config)# no ip route 172.16.1.0/24 192.168.1.1</td>

<td style="width: 297.767px;">SW(config)# ip route 172.16.1.0 255.255.255.0 192.168.1.1  
SW(config)# no ip route 172.16.1.0 255.255.255.0 192.168.1.1</td>

</tr>

<tr>

<td style="width: 134px;">Configure static route with administrative distance.</td>

<td style="width: 231.233px;">UBNT(config)# ip route 172.16.1.0/24 192.168.1.1 15</td>

<td style="width: 297.767px;">SW(config)# ip route 172.16.1.0 255.255.255.0 192.168.1.1 15</td>

</tr>

<tr>

<td style="width: 134px;">Configure/Remove null0(blackhole) route.</td>

<td style="width: 231.233px;">UBNT(config)# ip route 172.16.1.0/24 null0  
UBNT(config)# no ip route 172.16.1.0/24 null0</td>

<td style="width: 297.767px;">SW(config)# ip route 172.16.1.0 255.255.255.0 null0  
SW(config)# no ip route 172.16.1.0 255.255.255.0 null0</td>

</tr>

<tr>

<td style="width: 134px;">Configure/Remove ICMP reject route.</td>

<td style="width: 231.233px;">UBNT(config)# ip route 172.16.1.0/24 reject  
UBNT(config)# no ip route 172.16.1.0/24 reject</td>

<td class="wysiwyg-text-align-center" style="width: 297.767px;">N/A</td>

</tr>

</tbody>

</table>

<a name="18"></a>
