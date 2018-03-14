# orion360-sdk-pro-hello-ios
Repository for Orion360 SDK Pro for iOS, Hello

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
12. [Adding Orion360 SDK to our project](#adding-orion360-sdk-to-our-project)
13. [Start new Xcode session](#start-new-xcode-session)
14. [Working on OrionImageViewer xcworkspace](#working-on-orionimageviewer-xcworkspace)
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


