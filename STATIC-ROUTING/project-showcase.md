<h1>: STATIC-ROUTING</h1>


<h2>Description</h2>
<br>A Static Route is a manually configured path defined by a network administrator to direct traffic toward a specific destination network. Unlike dynamic routing, which uses protocols to discover paths automatically, static routing remains fixed unless a human manually changes the configuration.

## Key features of the implementation/Environments include:

- <B> SIMULATION SOFTWARE (Cisco Packet Tracer) Deployments to minimize hardware costs and physical space usage
- <B> CISCO ROUTER 2011
- <B> CISCO Switch 2960
- <B> PC's
- <B> Straight through cables
- <B> SERIAL CABLE


<h2>Project walk-through:</h2>

<p align="center">
Network Diagram: <br/>
<img src="https://imgur.com/D1tKMh6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
ADDING THE SERIAL-PORT:  <br/>
<img src="https://imgur.com/2y5W3uv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
CONFIGURING THE IP ADDRESS ON THE INTERFACE G0/0 AND BRINGING THE INTERFACE UP:  <br/>
<img src="https://imgur.com/WssMPqO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
CONFIGURING THE IP ADDRESS ON THE INTERFACE G0/1 AND BRINGING THE INTERFACE UP:  <br/>
<img src="https://imgur.com/W1IYSaK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
CONFIGURING THE IP ADDRESS ON THE INTERFACE S0/3/0 AND BRINGING THE INTERFACE UP:  <br/>
<img src="https://imgur.com/SYNjzeX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<BR />
  
  ## CONFIGURATION FOR ROUTER1
  
<br />
<BR />
CONFIGURING THE IP ADDRESS OF THE INTERFACE ON G0/0 FOR AND BRINGING THE INTERFACE UP :  <br/>
<img src="https://imgur.com/EowkuHV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
CONFIGURING THE IP ADDRESS OF THE INTERFACE ON G0/1 FOR AND BRINGING THE INTERFACE UP
<img src="https://imgur.com/j8yks1k.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
CONFIGURING THE IP ADDRESS ON THE INTERFACE S0/3/0 AND BRINGING THE INTERFACE UP:  <br/>
<img src="https://imgur.com/es2mliG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<BR />
CONFIGURING THE IP ROUTE (DESTINATION ADDRESS + SUBNET MASK + NEXT-HOP ADDRESS):  <br/>
<img src="https://imgur.com/BG0kMLI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> </BR>
<P1>CONFIGURING THE IP ROUTE CONTAINS THE DESTINATION ADDRESS/SUBNET-MASK AND THE NEXT-HOP ADDRESS.IT WOULD BE ABOUT THE ROUTER0 INFORMATION(THE OTHER ROUTER INFORMATION)</P1>
<br />
<BR />
CONFIGURING THE IP ROUTE (DESTINATION ADDRESS + SUBNET MASK + NEXT-HOP ADDRESS):  <br/>
<img src="https://imgur.com/y8aqqJg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> </BR>
<P1>CONFIGURING THE IP ROUTE CONTAINS THE DESTINATION ADDRESS/SUBNET-MASK AND THE NEXT-HOP ADDRESS FOR THE SECOND ROUTER CONTAINING THE INFORMATION OF THE OTHER ROUTER (ROUTER1) I.E ROUTER1 INFORMATION ON ROUTER0</P1>
<br />
<BR />
</p>

CONFIGURING THE IP ADDRESS AND GATEWAY TO THE PC'S AND PING EACH OTHER OR SEND PACKET FOR CONFIRMATION OF PROPER CONNECTION:  <br/>
<img src="https://imgur.com/Bw46qRO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

PINGING THE PC'S TO EACH OTHER:  <br/>
<img src="https://imgur.com/GxAJWFK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<h2>Conclusion</h2>

<br>In conclusion, static routing remains a fundamental and highly relevant concept in networking, despite the widespread adoption of dynamic and automated solutions. It offers unmatched control, predictability, and transparency, making it ideal for small networks, lab environments, and security-sensitive deployments. More importantly, understanding static routing builds the logical foundation required to design, troubleshoot, and optimize complex network infrastructures. This repository serves as a practical reference for mastering static routing principles, reinforcing core networking knowledge that every network engineer should possess.

<br />
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
