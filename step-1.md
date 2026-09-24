## Install Ubuntu 22.04.5 LTS 🐧

1. Download the IOS image here: https://ubuntu.com/download/server/thank-you?version=22.04.5&architecture=amd64&lts=true
2. Create a bootable USB flash drive with an image writer (Raspberry Pi Imager)
>[!NOTE] When selecting an operating system (OS) choose **Use custom**, and select the downloaded IOS image. 
4. Boot the newly created image from Raspberry Pi imager from the USB flash drive to the desired computer

## Update system package definitions and apply security packages:

> sudo apt update && sudo apt upgrade -y

## Install Core Xfce and LightDM (Display Manager): 

> sudo apt install --no-install-recommends xorg lightdm slick-greeter xfce4 -y

## Install Firefox 🦊

> sudo snap install firefox (or sudo apt install firefox)

## Set the Raspberry Pi to boot directly into the GUI:
