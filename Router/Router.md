# Router Configuratie

<details class="details-section">
	<summary class="section-summary">Router Configuratie</summary>

```
Configuratie : TechNova-Router

TechNova-Router#show running-config 
Building configuration...

Current configuration : 1461 bytes
!
version 15.4
no service timestamps log datetime msec
no service timestamps debug datetime msec
service password-encryption
security passwords min-length 8
!
hostname TechNova-Router
!
login block-for 60 attempts 3 within 60
!
!
enable secret 5 $1$mERr$5.a6P4JqbNiMX01usIfka/
!
!
!
!
!
!
no ip cef
ipv6 unicast-routing
!
no ipv6 cef
!
!
!
username sander secret 5 $1$mERr$4xjGwY49hVqWstBZT3bBv.
!
!
!
!
!
!
!
!
!
!
ip domain-name TechNova.com
!
!
spanning-tree mode pvst
!
!
!
!
!
!
interface GigabitEthernet0/0/0
description to switch develpors
ip address 192.168.0.1 255.255.255.224
duplex auto
speed auto
ipv6 address FE80::1:1 link-local
ipv6 address 2001:DB8:1::1/64
!
interface GigabitEthernet0/0/1
description connected to ADMIN-&-HR
ip address 192.168.0.33 255.255.255.224
duplex auto
speed auto
ipv6 address FE80::2:1 link-local
ipv6 address 2001:DB8:2::1/64
!
interface Vlan1
no ip address
shutdown
!
ip classless
!
ip flow-export version 9
!
!
ip access-list extended sl_def_acl
deny tcp any any eq telnet
deny tcp any any eq www
deny tcp any any eq 22
permit tcp any any eq 22
!
banner motd ^C

==========================================================

##########WARNING: Authorized Access Only ############

==========================================================
^C
!
!
!
!
line con 0
password 7 08315442000A09120700
login
!
line aux 0
!
line vty 0 4
password 7 08315442000A09120700
login
transport input ssh
!
!
!
end

```
</details>
