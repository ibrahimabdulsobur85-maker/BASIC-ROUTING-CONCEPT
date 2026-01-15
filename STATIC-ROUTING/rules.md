<h1>RULES OF STATIC ROUTING CONFIGURATION</h1>

  
## Rule 1: Interfaces must be UP before the route is added to the table.
<li>make sure all the interface are up berfore configuring ip route</li>

<h2>ROUTER CONFIGURATION (R1)</h2>

<li>Router0> enable</li>
<li>Router0# configure terminal</li>


<h3>Setup local interface (The 'Directly Connected' Rule)</h3>

<li>Router0(config)# interface gi0/0</li>
<li>Router0(config-if)# ip address 192.168.10.1 255.255.255.0</li>
<li>Router0(config-if)# no shutdown</li>
<li>Router0(config-if)# exit</li>

<h3>Setup outbound interface</h3>


<li>Router0(config)# interface gi0/1</li>
<li>Router0(config-if)# ip address 10.0.0.1 255.255.255.252</li>
<li>Router0(config-if)# no shutdown</li>
<li>Router0(config-if)# exit</li>

<h2>ROUTER CONFIGURATION (Router1)</h2>

<li>Router1> enable</li>
<li>Router1# configure terminal</li>


<h3>Setup local interface (The 'Directly Connected' Rule)</h3>

<li>Router1(config)# interface gi0/0</li>
<li>Router1(config-if)# ip address 192.168.20.1 255.255.255.0</li>
<li>Router1(config-if)# no shutdown</li>
<li>Router1(config-if)# exit</li>

<h3>Setup outbound interface</h3>


<li>Router1(config)# interface gi0/1</li>
<li>Router1(config-if)# ip address 10.0.0.2 255.255.255.252</li>
<li>Router1(config-if)# no shutdown</li>
<li>Router1(config-if)# exit</li>



<h3>APPLYING STATIC ROUTING RULES</h3>
<h2>Rule 2: You must have a return route for two-way communication.</h2>

<li>The ip route address should be the other destination LAN address and the next hop address of the router</li>

<h3>Rule: Destination + Mask + Next-Hop IP</h3>
<li>Router0(config)# ip route 192.168.20.0 255.255.255.0 10.0.0.2</li>

<li>Router1(config)# ip route 192.168.10.0 255.255.255.0 10.0.0.1</li>


<h3>VERIFICATION</h3>

<li>R1# show ip route</li>
<li>R1# show ip route static</li>
<li>R1# ping 192.168.20.1</li>
<li>R1# write memory</li>
