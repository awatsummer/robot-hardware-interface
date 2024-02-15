# robot-hardware-interface
** These instructions are for Windows 10 **

## Velodyne VLP-16
VLP-16 User Manual: https://velodynelidar.com/wp-content/uploads/2019/12/63-9243-Rev-E-VLP-16-User-Manual.pdf
### Necessary Installations:
1. VeloView Software:

VeloView is used to visualize the sensor data. To install the app, go to this link: https://www.paraview.org/veloview/#download
Scroll down to the "Download" section and select the correct version for your device.
Once downlaoded, open the installer and follow the instructions.

### Part 1 - Network Setup:
** DO THIS BEFORE CONNECTING ANYTHING **
1. Turn off Wifi
2. Open control panel
3. Click on "Network and Sharing"
4. Click on "Change adapter settings"
5. Click on wanted Ethernet network (will probably say "Not Connected")
6. Click on "Change Settings of this Network"
7. Scroll down on the first list shown and click on "Internet Protocol Version 4 (TCP/IPv4)
8. Click on "properties"
9. In the pop up, change the following:
   IP address: 192.168.1.222
   Subnet mask: 255.255.255.0
   ![image](https://github.com/awatsummer/robot-hardware-interface/assets/71294412/7a10301a-4217-463c-86b7-13bb905e96d2)
11. Click OK

## Part 2 - Connecting LiDAR:
Connect cords in this order:
1. Connect power cord to the sensor box (do not plug in yet!)
2. Connect LiDAR to the sensor box
3. Connect Ethernet cable to computer
4. Connect Ethernet cable to the sensor box
5. Plug in the power cord
6. Wait for the 2 green lights in the sensor box and the LiDAR to start buzzing (roughly 30 seconds)
7. Go to http://192.168.1.201
Web interface main configureation page should pop up.
![image](https://github.com/awatsummer/robot-hardware-interface/assets/71294412/62676907-b4c9-4e6c-8a91-38590d6f0566)

If it says not available, you may have configured the wrong Ethernet port so unplug ethernet cable and power cord; then go back to Network setup and try a different Ethernet port.

## Part 3 - VeloView Visualization of Sensor Data
1. Open VeloView app (if you have not installed it, see install instructions above)
2. Go to File-> Open -> Sensor Stream

 ![image](https://github.com/awatsummer/robot-hardware-interface/assets/71294412/d480f6dd-40fb-400b-a200-6e3e2c57ab1a)

4. Select "VLP-16" -> OK
You should start seeing sensor data on the screen:
 ![image](https://github.com/awatsummer/robot-hardware-interface/assets/71294412/323176f1-e637-4cb5-98bf-d3f3ec269e43)

If you don't see data, you may need to configure the Firewall settings to allow VeloView to be used:
1. Open "Windows Defender Firewall with advanced Security" (can find using search)
2. Click on "Inbound Rules" (on the left)
3. Scroll on the list until you see "veloview"
4. For each "veloview" in the list:
   4.1: Double click "veloview"
   4.2: Make sure "Enabled" is selected
   4.3: Click on "Allow the connection"
   4.4: Click OK
Once that is done, go back to VeloView and you should see sensor data.

