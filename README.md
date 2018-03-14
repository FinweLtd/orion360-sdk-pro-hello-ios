# orion360-sdk-pro-hello-ios
Repository for Orion360 SDK Pro for iOS, Hello

# # Beginner's Guide to Orion360 SDK (Pro) for iOS
<img width="174" alt="screen shot 2018-03-14 at 11 35 41" src="https://user-images.githubusercontent.com/36510685/37399225-c5736c9c-2789-11e8-9765-f125c9bdcfdc.png">

Orion360™ SDK Pro is a binary delivery of the Orion360 Engine for iOS and tvOS. The SDK includes Pro SDK engine & feature set. To list few of the many features:

-   Multiple Panoramas, Views & Cameras,
    
-   Multiple Video Sources,
    
-   Image & Video Sprites,
    
-   AR Mode,
    
-   Positional Audio,
    
-   Live / Adaptive HLS Streaming ,
    
-  Click [here](http://orion360.finwe.mobi/sdk/) to read more about our SDKs

The Orion360™ SDK Pro can be used for iOS projects using Swift and/or Objective-C.

This repository contains minimal 360° video player iOS application written in Swift. Video is playing from URL using OrionView’s default settings.

The example app :

   -  Plays one hardcoded 360x180 equirectangular video, 
   -  Auto-starts playback on load,
   -  Stops after playback is finished,
   -  Sensor fusion (acc+mag+gyro+touch),
   -  Panning (gyro, swipe),
   -  Zooming (pinch),
   -  Fullscreen view locked to landscape.

> Before using the SDK, read  [Licence Agreement](https://github.com/FinweLtd/Orion_SDK_iOS_SampleApps/blob/master/Finwe_Orion360_SDK_Basic_Evaluation_Kit_License_en_US-20161212_1500.pdf)

Table of Contents
-----------------
1. [Introduction](#introduction)
2. [Overview](#overview)
3. [Prerequisites](#prerequisites)
4. [Supported Devices](#supported-devices)
5. [Installation](#installation)
6. [CocoaPods installation guide](#cocoapods-installation-guide)
7. [Getting started with Xcode and creating new project](#getting-started-with-xcode-and-creating-new-project)
8. [Getting started with Podfile](#getting-started-with-podfile)
9. [Create Podfile](#create-podfile)
10. [Open Podfile in edit mode](#open-podfile-in-edit-mode)
11. [Edit the Podfile](#edit-the-podfile)
12. [Adding Orion360 SDK Pro to our project](#adding-orion360-sdk-pro-to-our-project)
13. [Start new Xcode session](#start-new-xcode-session)
14. [Working on OrionPro-VideoPlayer xcworkspace](#working-on-OrionPro-VideoPlayer-xcworkspace)
15. [Objective-C bridging header for Swift projects](#objective-c-bridging-header-for-swift-projects)
16. [Obtaining License File](#obtaining-license-file)
17. [Let us start to have fun with coding](#let-us-start-to-have-fun-with-coding)
18. [Run OrionImageViewer](#run-orionimageviewer)
19. [Next Steps](#next-steps)
20. [Feedback and support](#feedback-and-support)

## Introduction

The Orion360™ SDK Pro for iOS is a developer library to easily build and implement mobile applications that utilize immersive 360° video and 360° image content.

360° video/image is a special type of content that covers the complete surroundings of the camera. Using our SDK, 360° content can be included into mobile apps easily.

## Overview

The Orion360 SDK Pro for iOS provides a new iOS library that can be included to 3rd party iOS apps and that greatly simplifies building an app that supports 360° video/image content.

Using our SDK showing a single 360° video/image from the remote URL or from local file system requires only a few lines of code. This is achieved by providing a 360° video/image player component which enables the player to be simply dropped into a UI layout and initialized with a handler to 360° video/image.

## Prerequisites

The Orion360 SDK for iOS requires the standard development environment for iOS apps (Xcode Developer Tool).

## Supported Devices

Orion360 for iOS supports all iOS devices starting iOS version 7.0.

## Installation

The easiest way to take the SDK to use is to utilize the CocoaPods framework.
User manual is the best starting point for new users.
What is CocoaPods?

CocoaPods is the dependency manager which takes care of frameworks and third-party dependencies for your Xcode Projects. To use Orion360 SDK in your project, you need to install CocoaPods. Please follow installation guide below.

Note: If CocoaPods is already installed on your Mac you can skip this.

To check if CocoaPods is already installed or not, Open terminal and type the following command and press Return key (↵).

    pod install ↵

If CocoaPods is not installed, the following error log will be shown on terminal

-bash: pod: command not found

### CocoaPods installation guide

On terminal type, the following command and press Return key.

    sudo gem install cocoapods ↵

Note: Your machine might ask for your system password, type your password and press Return key. (Tip: you will not be able to see what you are typing while entering your password, make sure you press Return key after you finish entering your password). If the correct password is given CocoaPods will start the process of installation.

You can read more about CocoaPods and installation guide on: [http://guides.cocoapods.org/using/getting-started.html#installation](http://guides.cocoapods.org/using/getting-started.html#installation)
 
## Getting started with Xcode and creating new project

<img width="87" alt="screen shot 2018-02-27 at 13 14 21" src="https://user-images.githubusercontent.com/36510685/37399281-f0650852-2789-11e8-935d-eb5742af1d87.png">

Figure 1. Xcode Developer Tool

Open Xcode from the /Applications directory.

If this is the first time you’ve launched Xcode, it may ask you to agree to the user agreement and to download additional components. Follow the prompts through these screens until Xcode is completely set up and ready to launch.

As soon as Xcode launches, the welcome window appears (See Figure 2).

<img width="450" alt="screen shot 2018-02-27 at 13 17 38" src="https://user-images.githubusercontent.com/36510685/37399347-20ef2c82-278a-11e8-8bcf-e21a660473e4.png">

Figure 2. Xcode’s Welcome window

From the welcome window, click “Create a new Xcode project” (or choose File > New > Project). Xcode opens a new window (Figure 3) and displays a dialog in which you choose a template.

<img width="715" alt="screen shot 2018-02-27 at 13 30 56" src="https://user-images.githubusercontent.com/36510685/37399379-38239d48-278a-11e8-831d-f7f3ce1bdc5a.png">

Figure 3. Xcode’s window for choosing template

Select iOS from top of the dialog box and choose Single View App from Application section and then click Next to choose options for your project (Figure 4).

![screen shot 2018-03-14 at 12 59 58](https://user-images.githubusercontent.com/36510685/37399416-4c797682-278a-11e8-9226-04bd5e45c717.png)

Figure 4. Additional options for your project

In the dialog that appears (Figure 4), use the following values to name your app and choose additional options for your project:

-   Product Name:  OrionPro_VideoPlayer
    
-   Xcode uses the product name you entered to name your project and the app.
    
-   Team:  If this is not automatically filled in, set the team to None.
    
-   Organization Name:  The name of your organization or your own name. You can leave this blank.
    
-   Organization Identifier:  Your organization identifier, if you have one.
    
-   Bundle Identifier:  This value is automatically generated based on your product name and organization identifier.
    
-   Language:  Swift or Objective-C, depending on your preference. For this example, we are using Swift.
    
-   Devices: Universal
    
-   A Universal app is one that runs on both iPhone and iPad.
    
-   Use Core Data: Unselected.
    
-   Include Unit Tests: Unselected.
    
-   Include UI Tests: Unselected.
    

Click Next. In the dialog that appears, select a location to save your project and click Create.

Xcode opens your new project in the workspace window (See Figure 5).

<img width="719" alt="screen shot 2018-03-14 at 13 06 47" src="https://user-images.githubusercontent.com/36510685/37399499-7e9d10ba-278a-11e8-9e49-23557a4d8bb6.png">

Figure 5. OrionPro_VideoPlayer’s project workspace

As seen in Figure 5, CocoaPods is not yet added to our project. Step 2 of this documentation will guide you through CocoaPods and SDK installation.

## Getting started with Podfile

Go to terminal and navigate to project directory (OrionImageViewer). You can navigate using two ways. Either by navigating to project directory using cd \[type directory name\] or simply type cd and drag & drop your project directory on terminal and terminal will insert directory path for you, then press Return key (↵).

	cd <drag and drop your project folder> 

## Create Podfile

Type pod init and press Return key to create empty pod file for your project directory. Podfile is what you use to specify all the required libraries for your project. Type pod init command and press Return key (↵).

	pod init 

After running pod init Podfile is added to your project directory.

<img width="328" alt="screen shot 2018-03-14 at 13 10 18" src="https://user-images.githubusercontent.com/36510685/37399569-aad6833c-278a-11e8-97f2-a1fe964333d4.png">

Figure 6. OrionPro_VideoPlayer’s directory after pod init

## Open Podfile in edit mode

Type the following command on the terminal and press Return key (↵) to open Podfile in edit mode.

	open -e Podfile 

After opening the Podfile, you Podfile contents will look like Figure 7.

<img width="630" alt="screen shot 2018-03-14 at 13 11 56" src="https://user-images.githubusercontent.com/36510685/37399652-f184e382-278a-11e8-9f14-6ac572816555.png">

Figure 7. Podfile content before being edited

## Edit the Podfile

Edit the Podfile content as follows to Install Orion360 SDK Pro for iOS:

    source 'https://github.com/FinweLtd/orion360-sdk-pro-ios-specs.git'
    target 'OrionPro_VideoPlayer' do

    # Comment the next line if you're not using Swift and don't want to use dynamic frameworks
      use_frameworks!

      # Pods for OrionPro_VideoPlayer
      pod 'orion360-sdk-pro-ios'

    end

## Adding Orion360 SDK Pro to our project

After saving the updates you made on Podfile, go to terminal and type the following command and press Return key (↵)

	pod install 

After few minutes you will see a log something like Figure 8 on your terminal.

![screen shot 2018-03-14 at 13 29 00](https://user-images.githubusercontent.com/36510685/37399874-bb801f8a-278b-11e8-84cc-44b9c0c57a36.png)

Figure 8. Orion360 SDK installation completed

If you see message “Pod installation complete!”, you are ready to add our Orion360 SDK Pro to your project and start to have fun :)

Open project directory and you will see OrionPro_VideoPlayer.xcworkspace added (see Figure 9).

<img width="554" alt="screen shot 2018-03-14 at 13 31 46" src="https://user-images.githubusercontent.com/36510685/37400000-14559022-278c-11e8-92ff-07713a3db2a4.png">

Figure 9. Project directory’s content after successful pod installation

## Start new Xcode session

After successful pod installation, on the terminal you will see:
[!] Please close any current Xcode sessions and use `OrionPro_VideoPlayer.xcworkspace` for this project from now on.

<img width="113" alt="screen shot 2018-03-14 at 13 43 07" src="https://user-images.githubusercontent.com/36510685/37400476-be300144-278d-11e8-940c-0b12ba0f47e4.png">

Figure 10. OrionPro_VideoPlayer.xcworkspace

Notice: Whenever there will be a new update to the Orion360 SDK, go back to Step 2 and write pod update command and press Return key, and SDK will be updated right away.

	pod update 

## Working on OrionPro-VideoPlayer xcworkspace

After opening OrionImageViewer.xcworkspace you can see the SDK is successfully added to our project (see Figure 11).










--------------------------------------------
## Next Steps


It is recommended to get familiar with the [wiki](https://github.com/FinweLtd/OrionSDK_iOS_Prd/wiki) pages and API documentation that is included in the SDK to learn more about the available features and how they should be used.

Take a look at the delivered sample apps to get more familier with our SDK. Sample projects are done using Objective-C and Swift. 
Objective-C: [https://github.com/FinweLtd/orion360-sdk-pro-examples-ios](https://github.com/FinweLtd/orion360-sdk-pro-examples-ios), 
Swift: 

Clone the projects and follow steps mentioned in [Getting started with Podfile](#getting-started-with-podfile). 

Open .xcworkspace, build and run and project. Then look at the source code.

## Feedback and Support


Feedback & support should be directed via email to support@finwe.fi .
