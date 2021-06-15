# Touch_Haptic_Device_Drivers
Files and instructions for installing the Touch device drivers (Touch, Touch Stylus and Touch X). It has been tested with Touch USB device.

# Pre-requirements
Hardware:
- Touch device 

Software:
- Ubuntu 18.04

# Installation
  1. Install Dependencies
  
 ```
 sudo apt-get install --no-install-recommends freeglut3-dev g++ libdrm-dev libexpat1-dev libglw1-mesa libglw1-mesa-dev libmotif-dev libncurses5-dev libraw1394-dev libx11-dev libxdamage-dev libxext-dev libxt-dev libxxf86vm-dev tcsh unzip x11proto-dri2-dev x11proto-gl-dev x11proto-print-dev
 ```
 
 2. Download and Extract Openhaptics (v3.4) and Touch Haptic Device drivers: 
 
 Option 1.Using git 
 
 Option 2. Download manually

 
 4. Install OpenHaptics 
 ```
 cd ~/openhaptics_3.4-0-developer-edition-amd64/
 ```
 ```
 sudo ./install
 ```
 4. Install Touch Haptic Device Drivers
 
  ```
 cd ~/geomagic_touch_device_driver_2015.5-26-amd64/
 ```
 ```
 sudo ./install
 ```
 5. Execute the Touch Setup
 ```
 cd /opt/geomagic_touch_device_driver/ 
 ```
 ```
 ./Touch_setup
 ```
 6. Select and condigure your device. Then, click Apply and OK.
 7. Check if the device works correctly.

 ```
 ./Touch_Diagnostic
 ```
 Click **select** to open the rest of functionalities
