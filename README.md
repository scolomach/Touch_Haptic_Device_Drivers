# Touch_Haptic_Device_Drivers for Linux
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
 
 2. Download and Extract Openhaptics (v3.4)
 
 https://3dsystems.teamplatform.com/pages/102863?t=fptvcy2zbkcc
 
 3. Download and ExtractTouch Haptic Device drivers
 
 Option 1.Using git 
 
 The file is download in **Documents** file, but it can be another address or different file.
 
 ```
cd Documents
 ```
 
 ```
git clone https://github.com/scolomach/Touch_Haptic_Device_Drivers.git
 ```
 
 Option 2. Download manually

 
 4.1 Install OpenHaptics for Linux (download in: https://3dsystems.teamplatform.com/pages/102863?t=fptvcy2zbkcc)
 
 ```
 cd openhaptics_3.4-0-developer-edition-amd64/
 ```
 ```
 sudo ./install
 ```
 4.2 Install Touch Haptic Device Drivers for linux 

  ```
 cd Touch_Haptic_Device_Drivers/Touch_Drivers/
 ```
 ```
 sudo ./install
 ```
 5. Port device access (USB)

   5.1. Find out which port the haptic device has been assigned
  
 ```
 cd Documents/Touch_Drivers/
 ```
 ```
 bash ListUSBHapticDevices
 ```
 Normally, it returns **/dev/ttyACM0**.

   5.2. Give access

 ```
 sudo chmod 777 /dev/ttyACM0
 ```
 
 7. Execute the Touch Setup
 
 ```
 cd /opt/geomagic_touch_device_driver/ 
 ```
 ```
 ./Touch_setup
 ```
 6. Select and configure your device 
 
     Click **Apply** and **OK**.
 
 8. Check if the device works correctly

 ```
 ./Touch_Diagnostic
 ```
   Click **select** to open the rest of functionalities.
