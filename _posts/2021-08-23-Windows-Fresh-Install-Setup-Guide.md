---
layout: post
title: Windows Fresh Install Setup Guide
date: 2021-08-23 16:11
category: guides
author: Trevor Vance
tags: [guide, windows, setup]
summary: Guide to help setup Windows after a clean install.
---

This guide is intended to help setup a fresh install of Windows. Basically a personal checklist but I made it public so that other people can benefit from it as well.

**Note**: Any article linked in this guide will be followed by [[A](https://web.archive.org/)]. This is an Archive.org link through their [Wayback Machine](https://web.archive.org/) service. This allows me to save the exact state of the article. If in the future, any links break, the [[A](https://web.archive.org/)] can be used to see what I saw at the time of adding the article to this guide. I would still use the regular links first and keep the Wayback Machine link as a backup just in case they make any corrections that might be helpful.

# Obtain Windows to install
This guide is not intended to walk you through installing Windows, Just to setup a previously installed Windows. I included this as it might be helpful to some, but I'm not going to make a guide on the install process since it's been covered many times in other [guides](https://www.techradar.com/how-to/how-to-install-windows-10). [[A](https://web.archive.org/web/20210204010237/https://www.techradar.com/how-to/how-to-install-windows-10)]
- Use [Windows Media Creation Tool](https://go.microsoft.com/fwlink/?LinkId=691209) to download the latest iso straight from Microsoft or install it straight to your flashdrive.

# Updates
A fresh install of Windows will require updates. I suggest you follow the order of this guide and install these from top to bottom as they appear.

## Motherboard BIOS and Driver Updates
You should do this before anything else on your computer! BIOS first, but that can even be done before you reinstall Windows since it's installed directly to the motherboard and not your OS. The other downloads will be things like chipset drivers, on-board audio drivers, and LAN drivers. You don't have to install everything but don't just ignore what you don't know, look it up.
- Find your Motherboard make and model and search for that plus 'drivers'. For example, with the motherboard 'ASRock X570 Steel Legend' you will search for 'ASRock X570 Steel Legend drivers' and look for a page owned by the manufacturer. Look for a 'support', 'drivers', 'bios and firmware' or something of the sort. For the above example the page would be this: https://www.asrock.com/mb/AMD/X570%20Steel%20Legend/#Download

## Windows Updates
- Press the key combination: [Windows] + [I] to open Settings and go to Update & Security > Check for Updates.
-  If your installation media was too far behind (If you used the [Obtain Windows to install](#obtain-windows-to-install) section above it wont be.) updates can take a while. A good solution is to use [Windows Update Assistant](https://www.microsoft.com/en-us/software-download/windows10) to update your computer. After you update this way there might still be some smaller updates that need installed so do the bullet point right above this to be sure.

## Driver Updates
The above updates will get basic drivers for most, if not all, of your devices. Windows Update will install some generic drivers instead of ones from the manufacturer or even just older versions of the driver from the manufacturer. This section will show you how to make sure you have the optimal driver for your devices.

### Graphics Cards
Graphics Cards (known as GPU, Graphic Processing Unit, from here on) need the latest drivers installed to get the best performance for the latest AAA games. Rather than just install the drivers, I suggest to install what I'll call a driver maintainer for a lack of a better word. The purpose of a driver maintainer is to check the manufacturer periodically (usually daily) for a new driver to install so that you always have the latest installed when you want to play a game. If you are not going to play games I would still suggest always having the latest drivers. However, you can install the drivers without the driver maintainer. You should get the latest drivers from the manufacturer at least once on each install of Windows for a plethora of reasons.
- **Nvidia**
  - [**Nvidia Geforce Experience**](https://www.nvidia.com/en-us/geforce/geforce-experience/): Official driver maintainer for Nvidia Graphics card. Needs an Nvidia account but is very easy to use. 
  - [**NVCleanstall**](https://www.techpowerup.com/download/techpowerup-nvcleanstall/): Unofficial driver maintainer for Nvidia Graphics cards. Can give more privacy and possibly performance if you don't need some of the components that install on the Nvidia Geforce Experience drivers. Watch a video about this [here](https://www.youtube.com/watch?v=LR1XkjtylCM).
- **AMD**
  - [**AMD Radeon Software**](https://www.amd.com/en/technologies/radeon-software): I don't know of a NVCleanstall equivalent for AMD. I have used this pretty painlessly on my AMD GPUs from the past.

### Peripherals
A computer peripheral is any external device that provides input and output for the computer. [[source](https://techterms.com/definition/peripheral)] [[A](https://web.archive.org/web/20210414211113/https://techterms.com/definition/peripheral)] There is no way for me to know what peripherals you use. I will make a list of peripherals to think about but it will take a little work on your part to figure out what all drivers you need for your configuration. For gaming I highly recommended getting the latest driver for all peripherals to get the most performance out of each one. But, if you have a cheap/old device it might not have any drivers other than the generic and that's okay.
- **Mouse**: There are not that many things that it can help but if you play First Person Shooters then this can be really important! Non-gamers don't need to stress this.
- **Keyboard**: This is mostly going to help with configuration of RGB, macros, or other features that your keyboard might have. Many keyboards won't have any driver other than the generic ones that come with windows.
- **Monitor**: This might not really be necessary or even really a "driver" but I like to download the color profiles for my main monitor and install them to make sure the colors are *hopefully* the best that they can be. There might not be anything to download depending on the monitor but I'd suggest trying this, even for non-gamers.
- **Headset/Headphone/Microphone**: Audio is very important for gaming and other media consumption. I suggest getting the latest unless you plan to use no audio (unlikely). Audio drivers takes some understanding of how your audio is being processed, both input and output. The computer only knows 1's and 0's but we speak and hear in analog. This means that Audio coming in goes through an ADC (Analog to Digital Converter) and Audio coming out goes through a DAC (Digital to Analog Converter). Sometimes a DAC/ADC is built into the headset. You don't technically need drivers for the headset since it's just a microphone and some speakers, You need drivers for the DAC and ADC. 
  - **DAC/ADC Drivers**: The easiest way to figure out what you need is to look up the device followed by "drivers" (Make sure you are only clicking links from the official manufacturers website!). If you can't find anything, then it's fair to say it's probably using on-board audio. Another tell is if either or both of your audio input/output are connected to the motherboard via USB then you probably need to download drivers for that device. **Note**: It is possible to have headphones hooked up to an External DAC and a microphone using on-board audio or vice versa. In this case you would need separate drivers for each device.
  - **On-board Audio**: Your motherboard has audio input/outputs, usually on the back of your case exposed from the IO Shield and a second set that your case might expose by plugging into the motherboard. If your audio device is plugged into a 3.5 mm jack on the case or in the back of the motherboard OR if it's plugged into any other on-board audio (SPDIF or Optical for example) then the drivers you need are the audio drivers from the motherboard manufacturer that you should have grabbed in the [Motherboard BIOS and Driver Updates](#motherboard-bios-and-driver-updates) section above. If not, go back there now. 
- **Other**: There are so many peripherals that I can list here but each person will have different needs and therefore different peripherals. Basically, think about each USB that is plugged in and each PCI device on the motherboard, you may not have anything more than what is listed above. Think about whether each peripheral would benefit in any way from having the latest drivers. Here is a sample list of things that one might want to look for: Optical Disk Drive, Webcam, RGB Controller, StreamDeck, etc.

# Software Installs
This is highly subjective. I install more than this each time but I wanted to keep it more generalized so it doesn't get bulky, leaving you to wonder why I suggest you download so many programs that you might never use. I categorized it into three sections: General, Gaming, and Programming software. If you don't program, don't install from that section. If you don't play games, don't install from that section.
## General
- [**Ninite**](https://ninite.com/): This is one of my favorite tools. It's an installer for many different programs but isn't installed itself. Check the boxes for what you want installed and click the "Download Installer" button at the bottom. It will then download a small application that installs the checked programs and you can delete it forever! At a bare-minimum, I would suggest you grab 7-zip, Chrome AND Firefox (you never know when a site will work on one and not the other), and [Revo Uninstaller](https://www.revouninstaller.com/products/revo-uninstaller-free/) to help you remove programs in the future. I also like [Teracopy](https://www.codesector.com/teracopy) but that's a tool that not everyone might need.
  - [**Basic (non-gamer) config**](https://ninite.com/7zip-chrome-firefox-revo-teracopy/).
  - [**My personal config**](https://ninite.com/.net4.8-7zip-adoptjavax8-chrome-discord-firefox-googlebackupandsync-greenshot-pythonx3-revo-spotify-steam-teracopy-vlc-winscp-xnview/) (I recommend making your own with the first link)
- [**VS Code**](https://code.visualstudio.com/download) This program is geared towards programming but I use it for way more than that. Basically, anywhere I would have used notepad before, I use Code instead. You can edit config files, create text files, etc. **I do not install this from ninite** because it doesn't give the option to add to the context menu. Meaning that you can't right click a file and select "open with Code" which is helpful for looking at files of many types. 

## Gaming
- Install all of the game launchers that you use:
  - [**GOG Galaxy**](https://www.gog.com/galaxy)
  - [**Steam**](https://store.steampowered.com/about/) (I install this with ninite above)
  - [**Battle.net**](https://www.blizzard.com/en-us/apps/battle.net/desktop)
  - [**Ubisoft Connect**](https://ubisoftconnect.com/en-US/) (Formerly Uplay)
  - [**Origin**](https://www.origin.com/usa/en-us/store/download)
  - [**Epic Games**](https://www.epicgames.com/store/en-US/download) (I don't grab this one but I figured I'd include it)
 
## Programming
- [**Visual Studio**](https://visualstudio.microsoft.com/downloads/)
- [**WSL2**](https://docs.microsoft.com/en-us/windows/wsl/install-win10) [[A](https://web.archive.org/web/20210821102152/https://docs.microsoft.com/en-us/windows/wsl/install-win10)] (Windows Subsystem for Linux 2)
- [**Git**](https://git-scm.com/download/win)

# Windows Configurations
These configurations are things that I've had written down to remember each time but can be very important for gaming. I might add more categories later on but for now I only have important Gaming configs that I find myself using each time.
## Gaming
These are very important to remember for most gamers. 
- [Turn off](https://www.howtogeek.com/740365/how-to-turn-off-mouse-acceleration-on-windows-10/) [[A](https://web.archive.org/web/20210729023311/https://www.howtogeek.com/740365/how-to-turn-off-mouse-acceleration-on-windows-10/)] Mouse Acceleration. [Why](https://prosettings.net/library/what-is-mouse-acceleration/)? [[A](https://web.archive.org/web/20210125100220/https://prosettings.net/library/what-is-mouse-acceleration/)]
- [Change](https://support.microsoft.com/en-us/windows/change-your-display-refresh-rate-in-windows-c8ea729e-0678-015c-c415-f806f04aae5a) [[A](https://web.archive.org/web/20210709161535/https://support.microsoft.com/en-us/windows/change-your-display-refresh-rate-in-windows-c8ea729e-0678-015c-c415-f806f04aae5a)] your refresh rate. (If you have a monitor with a higher refresh rate than 60Hz)
