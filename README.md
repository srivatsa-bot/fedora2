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
```
10) Install Gnome Extensions - `dnf install chrome-gnome-shell gnome-extensions-app`
11) install kde connect - `sudo dnf install kdeconnectd`
 
