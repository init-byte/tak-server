## Install Ubuntu Server 22.04.5 LTS

1. Download the IOS image here: https://ubuntu.com/download/server/thank-you?version=22.04.5&architecture=amd64&lts=true
2. Create a bootable USB flash drive with an image writer (Raspberry Pi Imager)
>🛈 NOTE: When selecting an operating system (OS) choose **Use custom**, and select the downloaded IOS image. 
3. Boot the newly created image from Raspberry Pi imager from the USB flash drive to the desired computer

## Update system package definitions and apply security packages

`sudo apt update && sudo apt upgrade -y`

## Install Java OpenJDK 17

Check version:

`java --version`

If missing:

`sudo apt install openjdk-17-jre`

## Install Core Xfce and LightDM (Display Manager)

`sudo apt install --no-install-recommends xorg lightdm slick-greeter xfce4 -y`

Set the Raspberry Pi to boot directly into the GUI:

`sudo systemctl set-default graphical.target`

## Install Firefox 🦊

`sudo snap install firefox` or `sudo apt install firefox)`

## Install Xarchiver (the standard Xfce compression tool)

`sudo apt install xarchiver`

## Download Required Files

Download the following files from: https://tak.gov/products/tak-server

-	takserver-public-gpg.key
-	deb_policy.pol
-	takserver_x.x-RELEASExx_all.deb

