# locationtracker
Along with Location Information we also get **Device Information** without any permissions :

* Unique ID using Canvas Fingerprinting
* Device Model - Not always available
* Operating System
* Platform
* Number of CPU Cores - Approximate Results
* Amount of RAM - Approximate Results
* Screen Resolution
* GPU information
* Browser Name and Version
* Public IP Address
* Local IP Address
* Local Port

**Automatic IP Address Reconnaissance** is performed after the above information is received.

## How is this Different from IP GeoLocation

* Other tools and services offer IP Geolocation which is NOT accurate at all and does not give location of the target instead it is the approximate location of the ISP.

* Seeker uses HTML API and gets Location Permission and then grabs Longitude and Latitude using GPS Hardware which is present in the device, so Seeker works best with Smartphones, if the GPS Hardware is not present, such as on a Laptop, Seeker fallbacks to IP Geolocation or it will look for Cached Coordinates.  

* Generally if a user accepts location permsission, Accuracy of the information recieved is **accurate to approximately 30 meters**

* Accuracy depends on multiple factors which you may or may not control such as :
  * Device - Won't work on laptops or phones which have broken GPS
  * Browser - Some browsers block javascripts
  * GPS Calibration - If GPS is not calibrated you may get inaccurate results and this is very common

## Templates

Available Templates : 

* NearYou
* Google Drive
* WhatsApp 
* Telegram
* Zoom 
* Google reCAPTCHA 

## Tested On :

* Kali Linux
* BlackArch Linux
* Ubuntu
* Kali Nethunter
* Termux
* Parrot OS
* OSX - Monterey v.12.0.1

## Installation

### Kali Linux / Arch Linux / Ubuntu / Parrot OS / Termux

```bash
git clone https://github.com/Gokulkrish-CEH/Location-Tracker.git
cd Location-Tracker/
chmod +x install.sh
./install.sh
```

## cloudflare Tunnels
Use downlaod
```
Step1 : wget -q https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-linux-amd64.deb
Step2 : sudo dpkg -i cloudflared-linux-amd64.deb
Step3 : Sudo service apache2 start
Step4 : cloudflared --url localhost:8080
    
```
as an alterntive to ngrok

## Demo

**YouTube**

<a href="https://www.youtube.com/channel/UCXy84Xr78jA9sexgscO7GZA">
  <img src="https://dynamics365blocks.files.wordpress.com/2018/02/gps-tracking.png">
</a>
