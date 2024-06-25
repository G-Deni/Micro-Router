# Micro-Router
This project sets out to solve a simple but nitche problem, when using any form of hotspot in a large area covergae can suffer. Using a mesh-network of Micro-Routers coverage area can be extended for a short time without running any cables.
## Fetures 
Each Micro-Router uses a [Carambola2](https://www.8devices.com/products/carambola-2) SOM running [OpenWRT](https://openwrt.org/), A 3.3v TP4056 charging circut, and has serial output over USB-C using a CP2102N-Axx-xQFN20. There are exposed GPIO but acessing them requires a differnt top cover. 

**SOM:**

  [Carambola2](https://www.8devices.com/products/carambola-2)-NOTE this project uses the Carambola2 for its low poer draw on paper it should work with the Carambola3 at the cost of less runtime

**OS:**
<ul>
<li>OpenWRT<li>
</ul>

**Battery Capacity:**

  TBD
  
**Internaly exposed pins include:**
<ul>
  <li> 6 GPIO</li>
  <li>SPI Header</li>
  <li>Speaker - Uses one of the GPIO</li>
</ul> 

Ports include:
<ul>
  <li>USB-A - Media share capacity</li>
  <li>USB-C - Charging and UART</li>
  <li>2x RJ45 - LAN and WAN</li>
</ul>

## Docking Case
The Pcb layout may look rather unconvental but it is intental. The routers are optimed to be used in a dock configiuration. 
