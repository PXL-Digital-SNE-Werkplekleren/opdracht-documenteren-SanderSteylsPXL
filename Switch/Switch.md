# Switch Configuratie

<details class="details-section">
	<summary class="section-summary">Switch Configuratie</summary>

```
Configuratie: SW-DEV-01
SW-DEV-01#show running-config 
Building configuration...

Current configuration : 1967 bytes
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
service password-encryption
!
hostname SW-DEV-01
!
enable secret 5 $1$mERr$5.a6P4JqbNiMX01usIfka/
!
!
!
ip domain-name TechNova.com
!
username sander secret 5 $1$mERr$4xjGwY49hVqWstBZT3bBv.
!
!
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface FastEthernet0/1
description connected to PC1
!
interface FastEthernet0/2
description connected to PC2
!
interface FastEthernet0/3
description connected to PC3
!
interface FastEthernet0/4
description connected to PC4
!
interface FastEthernet0/5
description connected to PC5
!
interface FastEthernet0/6
description connected to PC6
!
interface FastEthernet0/7
description connected to PC7
!
interface FastEthernet0/8
description connected to PC8
!
interface FastEthernet0/9
description connected to PC9
!
interface FastEthernet0/10
description connected to PC10
!
interface FastEthernet0/11
description connected to PC11
!
interface FastEthernet0/12
description connected to PC12
!
interface FastEthernet0/13
!
interface FastEthernet0/14
!
interface FastEthernet0/15
!
interface FastEthernet0/16
!
interface FastEthernet0/17
!
interface FastEthernet0/18
!
interface FastEthernet0/19
!
interface FastEthernet0/20
!
interface FastEthernet0/21
!
interface FastEthernet0/22
!
interface FastEthernet0/23
!
interface FastEthernet0/24
!
interface GigabitEthernet0/1
!
interface GigabitEthernet0/2
!
interface Vlan1
ip address 192.168.0.2 255.255.255.224
!
ip default-gateway 192.168.0.1
!
banner motd ^C

==========================================================

##########WARNING: Authorized Access Only ############

==========================================================

^C
!
!
!
line con 0
password 7 08315442000A09120700
login
!
line vty 0 4
password 7 08315442000A09120700
login
transport input ssh
line vty 5 15
password 7 08315442000A09120700
login
transport input ssh
!
!
!
!
End

```
</details>
