# How to run QIRX on macOS using Crossover

QIRX (https://qirx.softsyst.com/) is a great SDR client that has been developed to run in its most full-featured form under Windows. Using Crossover, it's possible to run the full version of QIRX on macOS and presumably Linux. 

CrossOver (https://www.codeweavers.com/crossover) is a commercial version of Wine (https://github.com/wine-mirror/wine) with some additional UI features. Theoretically this should also work in the free version of Wine. 

![Hero Image](img/hero.png "Hero Image")
_Figure 0 - QIRX running on a Mac mini (2018) with 3.2GHz 6-Core Intel Core i7_

This configuration has been tested on a Mac mini (2018) with the lowest configuration, a 3.6Ghz Quad-Core Intel Core i3, as well as a Mac mini (2018) with a 3.2GHz 6-Core Intel Core i7 and a Macbook Air (M1, 2020) with an Apple M1 (a.k.a. "Apple Silicon" or "ARM64" architecture). It has also been tested on macOS Big Sur 11.6 and macOS Monterey 12.0.1. All configurations work with the same small issues which are documented below. 

## Prerequisites

These instructions assume that you have already configured a device as an rtl-tcp server. They also assume that you have installed CrossOver on your macOS device and have downloaded the QIRX Setup MSI file from https://qirx.softsyst.com/

## Step 1 - Load Crossover to the Installation Screen 
Click on Install a Windows Application
![alt text](img/Image1.png "Figure 1")

## Step 2 - Type in the name of the application to install
Type in QIRX and select it as an Unlisted application
![alt text](img/Image2.png "Figure 2")

## Step 3 - Click on Choose Installer File...
![alt text](img/Image3.png "Figure 3")

## Step 4 - Navigate to the QIRX Setup MSI file
In this example, the file is on the Desktop and we are installing QIRX version 3.1.7 using the file QIRX317_Setup.msi
![alt text](img/Image4.png "Figure 4")

## Step 5 - Click Continue
Once selected you will see the msi file and you can click Continue
![alt text](img/Image5.png "Figure 5")

## Step 6 - Select the New Windows 10 64-bit Bottle...
Although it may work with other bottle configurations, the best is to select a new Windows 10 64-bit Bottle
![alt text](img/Image6.png "Figure 6")

## Step 7 - Confirm all your settings and click Install
![alt text](img/Image7.png "Figure 7")

## Step 8 - Installation begins
If you are running some anti-virus software, it may complain about some of the files in the bottle. This is a known issue, the files are not malicious. Not all anti-virus software will do this.
![alt text](img/Image8.png "Figure 8")

## Step 9 - Click Next> at the first Wizard
![alt text](img/Image9.png "Figure 9")

## Step 10 - Read and agree the License Agreement
Click Next >
![alt text](img/Image10.png "Figure 10")

## Step 11 - Accept the default installation folder
Click Next >
![alt text](img/Image11.png "Figure 11")

## Step 12 - Create Desktop Icon
Click Next >
![alt text](img/Image12.png "Figure 12")

## Step 13 - Confirm Installation
Click Next >
![alt text](img/Image13.png "Figure 13")

## Step 14 - The Wizard should show successful completion
Click Close >
![alt text](img/Image14.png "Figure 14")

## Step 15 - The CrossOver Software Installer should show completion of QIRX
Click Done 
![alt text](img/Image15.png "Figure 15")

## Step 16 - The First Little Problem!
Crossover will install the software, but the icon will not be visible in the CrossOver screen.
![alt text](img/Image16.png "Figure 16")

## Step 17 - Double-Click on Run Command
You will need to run the `qirx.exe` application which (if you have the default configuration of CrossOver) can be found at `/Users/<youruser>/Library/Application Support/CrossOver/Bottles/QIRX/drive_c/Program Files/softsyst/QIRX3/qirx.exe` - Make sure to replace <youruser> with your actual username. Enter this path into the Command box and click on "Save Command as a Launcher" then Run. If you forget to click on "Save Command as a Launcher" you will have to repeat this process if you want a QIRX icon in CrossOver.
![alt text](img/Image17.png "Figure 17")
  
## Step 18 - Create the default config file
The first time you run `qirx.exe` you will be prompted to create a default config file. Click Yes.
![alt text](img/Image18.png "Figure 18")

## Step 19 - It Works!
You will next see QIRX start up, but with just the default empty configuration
![alt text](img/Image19.png "Figure 19")

## Step 20 - The Second Little Problem!
Click on the Gear at the top of the menu which will open up the Settings screen. For some reason this screen doesn't render properly and you can either end up with a completely black menu, a flashing menu or a menu missing the OK button. If it works, GREAT, if not, continue to Step XX to edit the config file manually. In my case, I entered the information for my rtl-sdr server in row 1. What you cannot see is that some of those columns are meant to have titles, the one to the left of Autostop is Autostart. I have them both disabled. The first checkbox after RTL-SDR determines whether that radio is enabled or not. For simplicity, enter the IP address and Port of your rtl-sdr server where I have done so and click OK. You will also get that QIRX Configuration notice, just click OK.
![alt text](img/Image20.png "Figure 20")
  
  
