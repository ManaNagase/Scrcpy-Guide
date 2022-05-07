# Scrcpy-Guide

**Please read this step by step(except mentioned otherwise), as i may mention something you aren’t aware of at any point**

**In this guide we’ll be using scrcpy & adb android platform tools**

**Do this at your own risk, I will not be held accountable for any damages you cause to your system**

**Note that this doesn’t run the game natively on your pc, it enables macroing and easier gameplay overall**

Stuff that you will need: Android phone (Sorry Apple Users), A pc and a Usb-a to Usb-c/Usb-mini cable (Basically your phone charger)

Depending on the OS you use for your pc you need a different tool, For windows you’ll need Scoop, for MacOs you’ll need Homebrew and Linux won’t need any extra installation tools You can actually use the web app for the program too at https://app.webadb.com (You only need to enable developer mode and the short tutorial on how to use the website)


**Enabling developer mode**

First off we need to enable developer mode on your phone. the process is very straightforward in most phones.
Open the settings app and search a tab called *About device*, *About phone* or something along those lines, inside About phone search for *Build number*, depending on your phone you might have to tap *Software information*, then tap *Build number*. You should at least tap it 10 times, but if you go over it doesn’t matter so I’d just spam it. Next thing it’ll ask for your pin/password/whatever for your phone, this is normal, as it wants you to confirm that you want to *enable Developer mode*.
If this doesn’t work for your phone model you can google “How to enable developer mode YourPhoneModel”


**Windows Tool Installation**

We are going to install scoop, scoop is a package manager for windows meaning it can install our dependencies.
What we’re gonna do to install it is go to the windows search bar, search for powershell, run it as administrator and paste this :

Invoke-Expression (New-Object System.Net.WebClient).DownloadString('https://get.scoop.sh')


Note: if you get an error you might need to change the execution policy (i.e. enable Powershell) with
Set-ExecutionPolicy RemoteSigned -scope CurrentUser

And just like that you have successfully installed scoop. Now we’re gonna install our main tools (you may switch to cmd for this if you don’t feel comfortable with powershell, it’s the same process), first we’re gonna run *scoop install adb* then we’re gonna run *scoop install scrcpy*


**Linux Install**

**Debian/Ubuntu Based**

run *apt install scrcpy* in terminal

Ubuntu:
If packages are not found, try running *sudo add-apt-repository universe* then *sudo add-apt-repository multiverse* then *sudo apt update*
You'll need the user password for that

**Arch based**

run *pacman -S scrcpy* in terminal


**MacOS Tool Installation**

We’re gonna be installing Homebrew https://brew.sh/
For macOS its better to have an administrator account but is no longer required. Just open up a command prompt and paste */bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"*
And just like that you have successfully installed homebrew, Now we’re gonna install our main tools, first we’re gonna run terminal and copy paste this > *brew install scrcpy* and then *brew install android-platform-tools*  these are the tools to capture the screen.


**Using scrcpy & adb**

Once you completed the tool installation run *adb devices* and you should see the serial number of the phone you plugged in (if it doesn’t show up please unplug and plug it again) and the word unauthorized, check your android device it will be asking to allow debugging and do you trust the device,then check your phone, and it’ll ask if you trust this device. You should press yes, in most phones there’s a checkbox that asks you if you trust this device (so the popup doesn’t happen when you try to run it on your pc), I’d press it bc it makes it easier, but it’s up to you

After that we’re gonna paste *adb devices* in the console and you will see your phone is no longer unauthorized, then you should be able to run in your console *scrcpy* or *scrcpy –print-fps* and just like that an app should open in your pc (it’ll take about 30 secs or so, it has to build the bridge), And There you have it, your phone's screen on your pc


**How to use the website**

Go to https://app.webadb.com, press the Add Devices Button and select your phone, Press connect and press the scrcpy button, and then press the play button

It'll give you a lower fps rate, please take that into account.

**Credits**

Credits to 112cxyz for helping me with the macOS & Linux Installation
