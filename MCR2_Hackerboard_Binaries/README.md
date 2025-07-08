
---
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/ManchesterRoboticsLtd/Puzzlebot/blob/main/Misc/Logos/Puzzle_Bot_Logo_W.png">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/ManchesterRoboticsLtd/Puzzlebot/blob/main/Misc/Logos/Puzzle_Bot_Logo_B.png">
  <img alt="Shows MCR2 logo in black or white." width="250" align="right">
</picture>

 <div id="user-content-toc">
  <ul align="center" style="list-style: none;">
    <summary>
      <h1>Puzzlebot: External Control configuration </h1>
    </summary>
  </ul>
</div>


---

# Instructions

The firmware utilities allow for flashing the puzzlebot firmware and LittleFS file system data on the ESP32 chip.

1. Download and unzip the full folder
2. Open the folder according to your OS
4. Connect the Hackerboard to the computer and Turn it ON
5. Make sure the Hackerboard is connected properly
6. Follow the instructions for each OS (plug and play)
7. Run the script files for the corresponding operating system (Windows, Linux, MacOS).

* **Linux**:

    * Run ./FirmwareFlash.sh  : flashes the firmware and data to the esp32, prompting the user for Network SSID and Password

    * Set permission to be executed in properties of firmware flash

* **Windows**:
  * Run (double click) FirmwareFlash.bat  : flashes the firmware to the esp32, with prompts for the Network SSID and password

* **MacOS**
  * Rub ./FirmwareFlash.sh  : flashes the firmware and data to the esp32

  * Set permission to be executed in properties to both files.



The binary files contain the default "config_live.json" configuration file.
The config file can be edited as follows:
 - connect to the robot access point;
 - open: "http://192.168.1.1/config";


## Troubleshoot


### Drivers I
* Drivers are usually installed automatically by Windows and Ubuntu even for the Virtual Machines.
* How do I know if the drivers are properly installed (Windows)?
* Plug the Puzzle-Bot into the USB port. 
* Go to Start > Device Manager
* The Serial port should appear as shown in the following figure (The COM port may vary).

![image](https://github.com/user-attachments/assets/89541ee4-b827-4fbd-9937-70bfadc89472)


* If the computer cannot find the drivers, download the drivers from the following link
[Drivers](https://ftdichip.com/drivers/vcp-drivers/)

* **Verify that the USB cable is a data cable and not only a power cable!**

* Scroll down and download the executable setup as shown in the following figure

![image](https://github.com/user-attachments/assets/6f6dc3d1-9bdc-4812-a6db-b1a9829b7c15)


### Before Installing the drivers!!
* Unplug the Puzzlebot from the computer.
* Unzip the drivers and run the setup (some computers must be restarted after the installation).
* Plug the Puzzlebot back into the computer.

### Drivers II
* Some Hackerboards have a different USB-UART chip the CP210x.
Drivers are usually installed automatically by Windows and Ubuntu even for the Virtual Machines.

* Verify if they are installed by following the steps in the previous slide.

* **Verify that the USB cable is a **data cable** and not only a power cable!**.

* If the computer cannot find the drivers, download the drivers from the following link [Drivers](https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers?tab=downloads)


### Drivers III
* My computer still not recognize the drivers even after the installation
* Plug the Puzzle-Bot into the USB port.
* Go to Start > Device Manager.
* Look for the USB Serial Converter as shown in the following picture.

![image](https://github.com/user-attachments/assets/2acc67ea-f417-44a0-a43a-e1d8c59b7c38)

* Right Click to Properties > Advanced Tab.
* Make sure the Load VCP box is checked.
* Reconnect the Puzzle-Bot to the computer.

![image](https://github.com/user-attachments/assets/07859b74-fa99-4a97-be46-94230f520b5d)
