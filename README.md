<p align="center">
  <img src="https://github.com/JamesMcCarthy79/Home-Assistant-Config/blob/master/HA%20Pics/Kingia%20Castle.png" width="250"/>
</p>
<h1 align="center">Kingia Castle Smart Home Configuration</h1>
<hr *** </hr>
<p align="center">Home Assistant Configuration &amp; Documentation for my Smart House.</p>
<p align="center">
  I live in <img src="https://github.com/oxguy3/flags/blob/master/mini/au.png"/>, and therefor my links are for where I purchased from. There may be better (and most likely cheaper) sites in your local regions.
</p>
<hr --- </hr>

### Smart Home Hardware Topology
<p align="center">
  <img src="https://github.com/JamesMcCarthy79/Home-Assistant-Config/blob/master/HA%20Pics/HA%20Topo.png"/>
</p>
<hr --- </hr>

<h3 align="left">Home Assistant Hardware</h3> 
<img src="https://github.com/JamesMcCarthy79/Home-Assistant-Config/blob/master/HA%20Pics/Rasp%20Pi%20Logo.png" width="200"/> 
<p align="left">There is nothing special regarding the hardware used when I start to notice available hardware resources becoming exhausted I will look to move to another platform. 
<hr --- </hr>


| [Raspberry Pi 3 Model B+](https://core-electronics.com.au/raspberry-pi-3-model-b-plus.html) | [Raspberry Pi 3 Model B+ Enclosure](https://core-electronics.com.au/raspberry-pi-3-case-enclosure.html) | [SandDisk Ultra 32GB Micro SD Card](https://www.officeworks.com.au/shop/officeworks/p/sandisk-ultra-32gb-micro-sdhc-memory-card-sdsq32gb) | [Raspberry Pi 3+ Power Supply](https://core-electronics.com.au/raspberry-pi-3-power-supply.html) |
| --- | --- | --- | --- |
| <img src="https://github.com/JamesMcCarthy79/Home-Assistant-Config/blob/master/HA%20Pics/raspberry-pi-3-model-b_-plus.png" width="250"/> | <img src="https://github.com/JamesMcCarthy79/Home-Assistant-Config/blob/master/HA%20Pics/Rasp%20Pi%20Case.png" width="250"/> | <img src="https://github.com/JamesMcCarthy79/Home-Assistant-Config/blob/master/HA%20Pics/Micro%20SD%20Card.png" width="200"/> | <img src="https://github.com/JamesMcCarthy79/Home-Assistant-Config/blob/master/HA%20Pics/Rasp%20Pi%20PSU.jpg" width="250"/> |

<h3 align="left">Home Assistant Software</h3>
<img src="https://github.com/JamesMcCarthy79/Home-Assistant-Config/blob/master/HA%20Pics/HA%20logo%202%20.png" width="200"/>
<p align="left">I have used Hassio with standard Add-On store packages which include Appdaemon for use with HaDashboard, Mosquitto Broker for MQTT Broker & Node-RED for more complex Automation flows.</p>
<hr --- </hr>

| [Hass.io](https://www.home-assistant.io/hassio/installation/) | [Mosquitto MQTT Broker](https://www.home-assistant.io/addons/mosquitto/) | [AppDaemon - HADashboard](https://www.home-assistant.io/docs/ecosystem/appdaemon/) | [Node-RED](https://github.com/notoriousbdg/hassio-addons/tree/master/node-red) |
| --- | --- | --- | --- |
| <img src="https://github.com/JamesMcCarthy79/Home-Assistant-Config/blob/master/HA%20Pics/HA%20logo.png" width="250"/> | <img src="https://github.com/JamesMcCarthy79/Home-Assistant-Config/blob/master/HA%20Pics/Mosquitto%20MQTT%20Logo.png" width="250"/> | <img src="https://github.com/JamesMcCarthy79/Home-Assistant-Config/blob/master/HA%20Pics/appdaemon.PNG" width="250"/> | <img src="https://github.com/JamesMcCarthy79/Home-Assistant-Config/blob/master/HA%20Pics/Node-RED%20Logo.png" width="250"/> |

<h4 align="left">Home Assistant:</h4>
<p align="left">As I am still new to Home Assistant (and always learning), I decided to install HASSIO. I have been using HASSIO since December 2017, for anyone new to HA I recommend this type of installation and once you are more comfortable with it I would then look to move onto some of the other methods of installation.</p>
<h4 align="left">MQTT Broker:</h4>
One of the first things I needed to do once I got HA up and running was to setup a MQTT Broker, I decided to use CloudMQTT(https://www.cloudmqtt.com/) as I found this really helpful guide from BRUH(https://www.youtube.com/watch?v=VaWdvVVYU3A) and was up and running in 15mins. The main problem I had with this method was using a cloud based service to control my mqtt based light switches. I decided to install Mosquitto Broker from the Hass.io Add-On Store. Doing this means I can host the MQTT Broker locally therefore having control of who can access my devices and data.
<h4 align="left">AppDaemon3 - HADashboard:</h4>
I have a bunch of wall mounted tablets (Android & IOS) aswell as RPi with 7" touchscreens and whilst I like the standard HA UI there is way too much going on for my wife and guests who need to interact with the smart home system. In cometh HADashboard, It wraps up your basic controls (lights, cooling, heating, music etc) into nice looking widgets that make using the smart home controls a breeze for any non tech person in the house (everyone but me). 
<h4 align="left">Node-RED:</h4>
After using HA for a few months I began to really enjoy the sometimes complicated methods of using automations, I also came to realise some of the limitations in its implementations. I found a really good repo with an easy to follow installation guide by NotoriousBDG here (https://github.com/notoriousbdg/hassio-addons/tree/master/node-red) this handles any of my more complicated flows and conditioning required for my Automations.
<hr --- </hr>

<h3 align="left">Kingia Castle Network</h3>
<img src="https://github.com/JamesMcCarthy79/Home-Assistant-Config/blob/master/HA%20Pics/Network%20Topo.png"/>
<p align="left">My Internet is a 100/40Mb/s FTTN solution where the fibre is terminated about 50m up the road and travels down phones lines (VDSL2+) for the remainder I typically acheive speeds of 92/35Mb/s. The core of my network switching devices are made up of Mikrotik Cloud Router Series, whilst my wireless network is comprised of both Altai and UBNT devices. I use a VPN and isolate my Smart Home devices from my Personal and Guest access networks through VLAN's and client isolation is implimented on the guest network.</p>
<hr --- </hr>

| [Core Router](https://mikrotik.com/product/CCR1009-7G-1C-PC) | [Core Switch](https://mikrotik.com/product/CRS125-24G-1S-IN) | [Upstairs Switch](https://mikrotik.com/product/CRS106-1C-5S) | [Cabling]() |
| --- | --- | --- | --- |
| <img src="https://github.com/JamesMcCarthy79/Home-Assistant-Config/blob/master/HA%20Pics/CCR1009.jpg" width="250"/> | <img src="https://github.com/JamesMcCarthy79/Home-Assistant-Config/blob/master/HA%20Pics/CRS-125.jpg" width="250"/> | <img src="https://github.com/JamesMcCarthy79/Home-Assistant-Config/blob/master/HA%20Pics/CRS106.png" width="250"/> | <img src="https://github.com/JamesMcCarthy79/Home-Assistant-Config/blob/master/HA%20Pics/Cabling.png" width="250"/> |

| [Altai A2c Dual-Band Access Point](https://www.powertec.com.au/altai-a2c-indoor-dual-band-2x2-802-11ac-ap-ceiling-mount) | [UBNT NanoBeam AC 5Ghz GEN2 19DBi](https://www.powertec.com.au/ubiquiti-nanobeam-ac-5ghz-gen2-19dbi-450mbps) | [UBNT NanoBeam AC 5Ghz GEN2 16DBi](https://www.powertec.com.au/ubiquiti-nanobeam-ac-5ghz-16dbi-450mbps) | [Network Management Tools]() |
| --- | --- | --- | --- |
| <img src="https://github.com/JamesMcCarthy79/Home-Assistant-Config/blob/master/HA%20Pics/Altai-A2c.jpg" width="250"/> | <img src="https://github.com/JamesMcCarthy79/Home-Assistant-Config/blob/master/HA%20Pics/Nano-19-AC.png" width="150"/> | <img src="https://github.com/JamesMcCarthy79/Home-Assistant-Config/blob/master/HA%20Pics/Nano-19-AC.png" width="150"/> | <img src="https://github.com/JamesMcCarthy79/Home-Assistant-Config/blob/master/HA%20Pics/Network%20Manage.png" width="250"/> |

<h4 align="left">Core Router:</h4>
<p align="left">My Core Router handles my PPPoE authentication, NAT and firewall rules. All of my remote access is handled by a build it Cloud DNS service on the Mikrotik Router along with an extensive list of non standard port forwards to gain access to every device I can remotley. I previously used the Mikrotik Device Tracker platform for online/offline status but found the response time too long so instead now use the Ping platform for device status monitoring.</p>
<h4 align="left">Core Switch:</h4>
<p align="left">My Core Switch is just a managed GBit Switch all of my ethernet connected devices connect to this via Cat6 in wall Cabling into Cat6 Wall plates and all use Cat6 Patch Cables.</p>
<h4 align="left">Wireless Access:</h4>
<p align="left">I have 4 SSID one for each of admin access, family access, guest access & smart home device access. I used to run a Cambium cnPilot E400 which I was given by Cambium for testing in a "Conference Environment" it was meant to be able to handle 100 similtaneous youtube streams well it started to fall over after about 35 connected clients (not streaming anything). Rather then filling the house with several APs I decided to go for the best in the business and am using a single Altai AP which is capable of handling 512 clients (currently have over 70 and still going strong). I only use 2.4G for access and have the 5G radio turned off as I use that spectrum for backhaul.</p>
<h4 align="left">Wireless PTMP Links:</h4>
<p align="left">I have a few impossible to cable areas of my 2 storey house (without running external ducting), between upstairs and downstairs and the outer wall of the downstairs area (where my media room is located). I have used a 19DBi UBNT NBE in AP mode connected directly to my Core Switch which links on 40Mhz channel to a unit in my media room and another upstairs which feeds into a Mikrotik switch that connects any ethernet devices upstairs</p>
<hr --- </hr>

<h3 align="left">Voice Control & TTS</h3> 

| <img src="https://github.com/JamesMcCarthy79/Home-Assistant-Config/blob/master/HA%20Pics/alexa.png" width="150"/> | <img src="https://github.com/JamesMcCarthy79/Home-Assistant-Config/blob/master/HA%20Pics/Kodi%20Logo.png" width="150"/> |
| --- | --- |
<p align="left">The voice control war has only just hit Australian shores, I dipped my toes into the Alexa waters a few years back with the original Echo and it was a bit of a flop due to nothing being supported in Australia. Once I moved to HA and its Amazon skill I dusted off the Echo and it has made my Smart come alive.</p>
<hr --- </hr>
