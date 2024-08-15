# fedora2

1) Dont mess with dns settings
2) Install rpm fusion from software.//code ins not needed
3) Flathub is official package manger in fedora. // code installation not needed
4) system update and app upgrade - ```sudo dnf -y update```  ```sudo dnf -y upgrade --refresh```
5) media codecs to open h264 refer this
   ```https://github.com/devangshekhawat/Fedora-40-Post-Install-Guide/blob/main/README.md```
7)Install GNOME Tweak Tool: `sudo dnf install gnome-tweak-tool`
8) own risk - preload - `sudo dnf copr enable elxreno/preload -y && sudo dnf install preload -y`
9) Firefox Tweaks. turn on the below settings:
```
about:config
layers.acceleration.force-enabled
gfx.webrender.all

settings - turn on dram
```
10) Install Gnome Extensions - `dnf install chrome-gnome-shell gnome-extensions-app`
11) install kde connect - `sudo dnf install kdeconnectd`
12) touch pad scrolling issue
   ```
To half your current touchpad scroll speed with a keypad size of 130mm x 80mm, you'll want to halve these dimensions. Here’s how to do it step by step:

### Steps to Halve the Scroll Speed:

1. **Calculate New Dimensions:**
   - Half of 130mm is 65mm.
   - Half of 80mm is 40mm.
   - So, your new dimensions will be 65mm x 40mm.

2. **Install `libinput-tools` (if not already installed):**
   - On Fedora, install the package with:
     ```bash
     sudo dnf install libinput-utils
     ```

3. **Run the Measurement Command:**
   - Use the following command to adjust the scroll speed:
     ```bash
     sudo libinput measure touchpad-size 65x40
     ```

4. **Test the Configuration:**
   - After running the command, move your fingers around the touchpad to check the functionality. Press `Ctrl + C` to stop the measurement once you're satisfied.

5. **Copy the Configuration Text:**
   - The terminal will display some configuration text. Copy the text found between the markers (usually `-8<------`).

6. **Create a Configuration File:**
   - As root, create a new file to store the custom configuration:
     ```bash
     sudo nano /etc/udev/hwdb.d/61-evdev-local.hwdb
     ```
   - Paste the copied configuration text into this file, then save and close the editor (use `Ctrl + O` to save and `Ctrl + X` to exit in nano).

7. **Update the Hardware Database:**
   - Apply the new configuration by updating the hardware database:
     ```bash
     sudo systemd-hwdb update
     ```

8. **Trigger the Changes:**
   - Reload the device configuration with:
     ```bash
     sudo udevadm trigger /dev/input/event*
     ```

9. **Reboot the System:**
   - Reboot your system to apply the changes:
     ```bash
     sudo reboot
     ```

### Final Steps:
- After rebooting, the scroll speed should be slower. If the cursor speed has also changed, you can adjust it in your system settings to your preference.

If you find that the scroll speed is still not ideal, you can repeat the process and further adjust the dimensions as needed.
```
my touch pad size is 130 X 80mm. i want to decrease the scrool speed by 60% so my value are 65 X 40. turn on touchpad accelaration in tweaks for better experience.

13) Dual boot bluetooth issue - `https://www.youtube.com/watch?v=BprSnu6KWTA`



***FOR CODING***
1) dont need to install python comes by default
2) to insatll c/cpp - `sudo dnf install gcc-c++ -y`. to verify do `gcc --version` in terminal
3) java comes pre installed too, you need to set java path manually.
4) install node - `sudo dnf install nodejs`. verify `node --version` `npm --version`
5) 


