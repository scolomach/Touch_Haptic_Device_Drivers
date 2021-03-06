# Touch_Haptic_Device_Drivers for Linux
Files and instructions for installing the Touch device drivers (Touch, Touch Stylus and Touch X). It has been tested with Touch USB device.


# Pre-requirements
Hardware:
- Touch device 

Software:
- Ubuntu 18.04

# Installation
  0. Install Qt (if the user does not have)
 ```
 sudo apt-get install qt5-default
 ```
  1. Install Dependencies
  
 ```
 sudo apt-get install --no-install-recommends freeglut3-dev g++ libdrm-dev libexpat1-dev libglw1-mesa libglw1-mesa-dev libmotif-dev libncurses5-dev libraw1394-dev libx11-dev libxdamage-dev libxext-dev libxt-dev libxxf86vm-dev tcsh unzip x11proto-dri2-dev x11proto-gl-dev x11proto-print-dev
 ```
 
 2. Download and Extract Openhaptics (v3.4)
 
 https://3dsystems.teamplatform.com/pages/102863?t=fptvcy2zbkcc
 
 3. Download and ExtractTouch Haptic Device drivers
 
 Option 1.Using git 
 
 The file is downloaded in **Documents** file, but it can be another address or different file.
 
 ```
cd Documents
 ```
 
 ```
git clone https://github.com/scolomach/Touch_Haptic_Device_Drivers.git
 ```
 
 Option 2. Download manually

 
 4.1 Install OpenHaptics for Linux (downloaded in: https://3dsystems.teamplatform.com/pages/102863?t=fptvcy2zbkcc)
 
 Go to the folder downloaded
 ```
 cd openhaptics_3.4-0-developer-edition-amd64/
 ```
 ```
 sudo ./install
 ```
 4.2 Install Touch Haptic Device Drivers for linux 

 Go to the folder downloaded
  ```
 cd Touch_Haptic_Device_Drivers/
 ```
 ```
 chmod 777 install
 ```
 ```
 sudo ./install
 ```
 5. Port device access (USB)

   5.1. Find out which port the haptic device has been assigned
  
 ```
 cd Documents/Touch_Haptic_Device_Drivers/
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
 ./Touch_Setup
 ```
 6. Select and configure your device 
 
     Click **Apply** and **OK**.
 
 8. Check if the device works correctly

 ```
 ./Touch_Diagnostic
 ```
   Click **select** to open the rest of functionalities.
   
# Problems
   1. If the device position is constant and your OS language is not English, consider changing locales.
  ```
  LC_NUMERIC=en_US.UTF-8
  LANG=en_US.UTF-8
  LC_ALL=en_US.UTF-8
   ```
   Logout and login again for the environmental variables to take effect use the command:
   ```
   gnome-session-quit
   ```
       
 
