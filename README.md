# Micro-Router
This project sets out to solve a simple but nitche problem, when using any form of hotspot in a large area covergae can suffer. Using a mesh-network of Micro-Routers coverage area can be extended for a short time without running any cables. This is achived by a custom OpenWRT configuration and a onboard battery that should yeild ~16hrs of run time.

![alt text](https://github.com/G-Deni/Micro-Router/blob/main/IMAGES/TOP-RENDER.png)


## Fetures 


### SOM
Each Micro-Router uses a [Carambola2](https://www.8devices.com/products/carambola-2) SOM running [OpenWRT](https://openwrt.org/). 


### Ports
<ul>
  <li>USB-A - Media share capacity</li>
  <li>USB-C - Charging and UART</li>
  <li>2x RJ45 - LAN and WAN</li>
</ul>

### Charge Controller
Powered A 3.3v TP4056 charging circut with a seperate 5v boost converter to power the USB-A port. The charge controller was selected for this project to be cheap, this means while the battery is protected there is no communication between the SOM and the charge controler. There is no safe start of shut down if the battery dies the charge conttroler will disconect the battery from the loads. It power switch toggles the boost converters on and off, disconnecting the battery from all loads at the boost converter. The 5v and the 3.3v boost converters are both 500mah and toggled on and off by the same slide switch.


### USB Serial
It has serial output over USB-C to help prevent bricking during development. All of the reset and clock pins are connected to make it as robust as possible, however if there is a problem with the serial connection both the Carambola2 and the serial to USB IC have reset pushbuttons. 


### GPIO/SPI Headers
Exposed on the board are two 2.25mm pitch headers one is for SPI screen output (four pin) and one for general GPIO (6 pin).  


### External Antenna
A board mounted SMA connecotr is impeadence matched for 2.4ghz wifi is exposed for a external antenna to be connected to. There is no internal antenna as the porfomance is ushually very poor.


### Speaker
Two pins are exposed for the speaker one is ground the other is a GPIO. One of the GPIO pins has to be resved to be used as a speaker. If the extra gpio pin is needed do not poluate the speaker.

## Docking Case
The Pcb layout may look rather unconvental but it is intental. The routers are optimed to be used in a dock configiuration. 
