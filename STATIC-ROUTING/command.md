<H1> BASIC STATIC ROUTING CONFIGURATION COMMAND</H1>
  
<H2>NETWORK TOPOLOGY: Router0 (10.0.0.1) <---> Router1 (10.0.0.2)</H2>

  
## Goal: Allow LAN-A (192.168.10.0) to communicate with LAN_B (192.168.20.0)
  
## ROUTER0 CONFIGURATION

  <LI>Router0> enable</LI>
<LI>Router0# config t</LI>

<H3>Configure Local LAN Interface</H3>


<LI>Router0(config)# interface GigabitEthernet0/0</LI>
<LI>Router0(config-if)# ip address 192.168.10.1 255.255.255.0</LI>
<LI>Router0(config-if)# no shutdown</LI>
<LI>Router0(config-if)# exit</LI>

<H3>Configure WAN Interface (Connection to Router_B)</H3>


<LI>Router0(config)# interface GigabitEthernet0/1</LI>
<LI>Router0(config-if)# ip address 10.0.0.1 255.255.255.252</LI>
<LI>Router0(config-if)# no shutdown</LI>
<LI>Router0(config-if)# exit</LI>


## ROUTER1 CONFIGURATION

<LI>Router1> enable</LI>
<LI>Router1# configure terminal</LI>

<H3>Configure Local LAN Interface</H3>
<LI>Router1(config)# interface GigabitEthernet0/0</LI>
<LI>Router1(config-if)# ip address 192.168.2.1 255.255.255.0</LI>
<LI>Router1(config-if)# no shutdown</LI>
<LI>Router1(config-if)# exit</LI>

<H3>Configure WAN Interface (Connection to Router_A)</H3>


<LI>Router1(config)# interface GigabitEthernet0/1</LI>
<LI>Router1(config-if)# ip address 10.0.0.2 255.255.255.252</LI>
<LI>Router1(config-if)# no shutdown</LI>
<LI>Router1(config-if)# exit</LI>


## STATIC ROUTE: Path to LAN-B via Router-B's IP
<LI>Router0(config)# ip route 192.168.20.0 255.255.255.0 10.0.0.2</LI>


## STATIC ROUTE: Path to LAN-A via Router-A's IP
<LI>Router1(config)# ip route 192.168.10.0 255.255.255.0 10.0.0.1</LI>

## VERIFICATION

<LI>Router0# show ip route static</LI>
<LI>Router0# ping 192.168.20.1</LI>
