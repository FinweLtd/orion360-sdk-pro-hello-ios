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
14. [Working on OrionPro-VideoPlayer xcworkspace](#working-on-orionpro-videoplayer-xcworkspace)
15. [Objective-C bridging header for Swift projects](#objective-c-bridging-header-for-swift-projects)
16. [Obtaining License File](#obtaining-license-file)
17. [Let us start to have fun with coding](#let-us-start-to-have-fun-with-coding)
18. [Run OrionPro-VideoPlayer](#run-orionpro-videoplayer)
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

As seen in Figure 5, CocoaPods is not yet added to our project. This documentation will guide you through CocoaPods and SDK installation.

## Getting started with Podfile

Go to terminal and navigate to project directory (OrionPro_VideoPlayer). You can navigate using two ways. Either by navigating to project directory using cd \[type directory name\] or simply type cd and drag & drop your project directory on terminal and terminal will insert directory path for you, then press Return key (↵).

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

Edit the Podfile content as follows to Install Orion360 SDK Pro for iOS.

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

Figure 8. Orion360 SDK Pro installation completed

If you see message “Pod installation complete!”, you are ready to add our Orion360 SDK Pro to your project and start to have fun :)

Open project directory and you will see OrionPro_VideoPlayer.xcworkspace added (see Figure 9).

<img width="554" alt="screen shot 2018-03-14 at 13 31 46" src="https://user-images.githubusercontent.com/36510685/37400000-14559022-278c-11e8-92ff-07713a3db2a4.png">

Figure 9. Project directory’s content after successful pod installation

## Start new Xcode session

After successful pod installation, on the terminal you will see:
[!] Please close any current Xcode sessions and use `OrionPro_VideoPlayer.xcworkspace` for this project from now on.

<img width="113" alt="screen shot 2018-03-14 at 13 43 07" src="https://user-images.githubusercontent.com/36510685/37400476-be300144-278d-11e8-940c-0b12ba0f47e4.png">

Figure 10. OrionPro_VideoPlayer.xcworkspace

Notice: Whenever there will be a new update to the Orion360 SDK Pro, go back to [Getting started with Podfile](#getting-started-with-podfile) step and write pod update command instead of pod install and press Return key, and SDK will be updated right away.

	pod update 

## Working on OrionPro-VideoPlayer xcworkspace

After opening OrionPro_VideoPlayer.xcworkspace you can see the SDK is successfully added to our project (see Figure 11).

![screen shot 2018-03-14 at 13 48 42](https://user-images.githubusercontent.com/36510685/37400734-80a6c758-278e-11e8-958b-8cd4f1fb9a07.png)

Figure 11. OrionPro_VideoPlayer’s project structure after pod install

The Orion360 SDK Pro can be used for both Objective-C and swift project. For Objective-C project you simply import OrionView (#import <orion360-sdk-pro-ios/OrionView.h>) header and initialize it as follows:

	OrionView *orionView = [[OrionView alloc] initWithFrame:CGRectMake(0, 0, self.view.bounds.size.width, self.view.bounds.size.height)]; 
	orionView.delegate = self;
  
Note that the license file need to be given.

	NSString *licenseFile = [NSString stringWithFormat:@"license.key.lic"];
	NSString* path = [[NSBundle mainBundle] pathForResource:licenseFile ofType:nil];
	NSURL *licenseUrl = [NSURL fileURLWithPath:path];
	[orionView setLicenseFileUrl:licenseUrl];

For Swift projects you need to create [Objective-C bridging header for Swift projects](#objective-c-bridging-header-for-swift-projects) to use OrionSDK Pro. For Objective-C projects, skip Objective-C bridging step and jump to [Obtaining License File](#obtaining-license-file) to learn how you can acquire Orion360 SDK Pro license file.

## Objective-C bridging header for Swift projects

Create bridging header as follows:

File > New > File > (iOS, watchOS, tvOS, or macOS) > Source > Objective-C File

![screen shot 2018-02-21 at 12 18 24](https://user-images.githubusercontent.com/36510685/37401202-fa412ec2-278f-11e8-99a1-e45485851d83.png)

Figure 12. Create new Objective-C file for bridging header

![screen shot 2018-03-14 at 14 01 32](https://user-images.githubusercontent.com/36510685/37401292-46e47a68-2790-11e8-9c98-4c5946fe41c6.png)

Figure 13. Create new Objective-C file for bridging header

Give file name which is similar to your project name for this example "OrionPro_VideoPlayer" and press Next, and save it in the same directory as your project.

If you accept, Xcode creates the header file along with the file you were creating, and names it by your product module name followed by "-Bridging-Header.h". When you press Create you will see a dialog message (see Figure 14) and click on “Create Bridging Header”.

![screen shot 2018-02-21 at 12 23 12](https://user-images.githubusercontent.com/36510685/37449105-b8d6be64-2831-11e8-9e35-7b068a101dc9.png)

Figure 14. Creating bridging header

![screen shot 2018-03-14 at 14 05 09](https://user-images.githubusercontent.com/36510685/37401449-bfafa8e6-2790-11e8-867c-74a0302a3584.png)

Figure 15. OrionPro_VideoPlayer’s project structure after creating bridging header

Now open OrionPro_VideoPlayer-Bridging-Header and type import "orion360-sdk-pro-ios/OrionView.h" and save the file. 

![screen shot 2018-03-14 at 14 06 48](https://user-images.githubusercontent.com/36510685/37401527-f924659e-2790-11e8-8fcf-2a54fb737969.png)

Figure 16. Importing Orion360 SDK Pro using import statement

After creating bridging header find the class line, which should look like this: class ViewController: UIViewController {

After UIViewController, add a comma (,) and OrionViewDelegate, OrionVideoContentDelegate and initialize OrionView as follows:

	let orionView = OrionView(frame: CGRect(x: 0, y: 0, width: view.bounds.size.width, height: view.bounds.size.height))  
	orionView.delegate = self

And license file is given as follows:

	let licenseFile = "Orion360_SDK_Pro_iOS_Trial_fi.finwe.OrionVideoPlayer.lic"
        let path: String? = Bundle.main.path(forResource: licenseFile, ofType: nil)
	let licenseUrl = URL(fileURLWithPath: path ?? "")
	orionView.licenseFileUrl = licenseUrl

## Obtaining License File

To show 360° content you need a license file that must be added to your app project's resources without any modification. Failure to do so will result to black video player screen and currently, it doesn't produce any warning messages.

Orion360 SDK Pro is a commercial product and requires a license file to work. An evaluation license is provided with the sample app. You can get a watermarked evaluation license file also for your own bundle identifier by creating an account to [https://store.make360app.com](https://store.make360app.com/), starting a new SDK project, providing your own package name, and selecting FREE Trial.

Please follow the steps below to obtain License File:
1.  Go to  [https://store.make360app.com](https://store.make360app.com/).
    
2.  Sign in if you have an existing account with us or Sign up if you are a new user.
    
3.  After successful login click on New SKD Project button.
<img width="150" alt="screen shot 2018-03-14 at 14 15 35" src="https://user-images.githubusercontent.com/36510685/37401873-36820558-2792-11e8-9a0b-ca3d8ce72e6b.png">

4.  Give Project Name, and Package Identifier as they are written on Identity section.    
![screen shot 2018-03-14 at 14 18 48](https://user-images.githubusercontent.com/36510685/37402014-aae68ab8-2792-11e8-99c1-275f6b85d9f2.png)

Figure 17. Select your project from target

Click on your project from Project Navigator > Select your target > choose General > Identify

<img width="701" alt="screen shot 2018-03-14 at 14 30 00" src="https://user-images.githubusercontent.com/36510685/37402494-7a07b1c2-2794-11e8-9347-a91c18c4f364.png">

Figure 18. Bundle Identifier = Package Identifier, Display Name = Project Name

5.  Select iOS on Platforms section.

<img width="504" alt="screen shot 2018-03-14 at 14 33 11" src="https://user-images.githubusercontent.com/36510685/37402589-dde8fbec-2794-11e8-9f73-7098c4b9336f.png">

Figure 19. Target platforms

6.  Choose type of license, payment method.

<img width="236" alt="screen shot 2018-03-14 at 14 36 26" src="https://user-images.githubusercontent.com/36510685/37402662-1dc6364e-2795-11e8-9e6f-17e8d9ac2006.png">

Figure 20. Payment method

And click on Free Trial or Purchase.

7.  Read and agree to our terms and regulations.
    

Click on Accept after reading Orion360 SDK Basic Evaluation End-User License Agreement (EULA)

![screen shot 2018-02-21 at 13 21 59](https://user-images.githubusercontent.com/36510685/37403063-4c8283ec-2796-11e8-9d8c-d5de7c14e218.png)

Figure 21. Orion360 SDK’s EULA

Once again click Accept to Terms & Conditions.

![screen shot 2018-02-21 at 13 23 11](https://user-images.githubusercontent.com/36510685/37403078-59450190-2796-11e8-82a0-73443bd87fe9.png)

Figure 22. Orion360 SDK’s Terms & Conditions

After accepting both terms, you will get a notification which says “Your new licenses are ready to be downloaded. Scroll down to the Downloads section to get them”.

<img width="351" alt="screen shot 2018-03-14 at 14 37 52" src="https://user-images.githubusercontent.com/36510685/37403242-d4438eb6-2796-11e8-960f-4e378c61afc1.png">

Figure 23. Downloads for extracted license

Click on “Download iOS Pro Trial License”.

8.  Add the downloaded license to your project
   
Extract the download file.  
Select “Orion360_SDK_Pro_iOS_Trial_fi.finwe.OrionPro-VideoPlayer.lic“, drag the file and drop it inside Project navigator under your project folder and click Finish.

![screen shot 2018-03-14 at 14 56 48](https://user-images.githubusercontent.com/36510685/37403629-276fb9ba-2798-11e8-858e-b0a9b6d3dd96.png)

Figure 24. Adding license file (.lic) to project directory

![screen shot 2018-03-14 at 14 57 16](https://user-images.githubusercontent.com/36510685/37403633-29cbd784-2798-11e8-8fc4-a6410a098e92.png)

Figure 25. Project structure after license file added

## Let us start to have fun with coding
Swift

	//  ViewController.swift
	//  OrionPro_VideoPlayer
	//
	//  Created by Tewodros Mengesha on 14/03/2018.
	//  Copyright © 2018 Finwe Ltd. All rights reserved.
	//

	/**
	 * OrionPro_Player implements a minimal Orion video player. It plays
	 * a video file from url using OrionView's default settings.
	 *
	 * Features:
	 * - Plays one hardcoded 360x180 equirectangular video
	 * - Auto-starts playback on load
	 * - Stops after playback is finished
	 * - Sensor fusion (acc+mag+gyro+touch)
	 * - Panning (gyro, swipe)
	 * - Zooming (pinch)
	 * - Fullscreen view locked to landscape
	 */

	import UIKit
	import Foundation

	class ViewController: UIViewController, OrionViewDelegate, OrionVideoContentDelegate{

	    var orionView: OrionView!
	    var videoContent: OrionVideoContent!
	    var viewPort: OrionViewport!
	    override func viewDidLoad() {
		super.viewDidLoad()
		// Do any additional setup after loading the view, typically from a nib.

	    }

	    override func didReceiveMemoryWarning() {
		super.didReceiveMemoryWarning()
		//view.backgroundColor = UIColor.clear
		// Dispose of any resources that can be recreated.
	    }
	    override func viewDidAppear(_ animated: Bool) {
		super.viewDidAppear(animated)


		if orionView == nil {

		    //Create an instance of OrionView
		    orionView = OrionView()
		    orionView.delegate = self
		    orionView.frame = CGRect(x: 0, y: 0, width: view.bounds.size.width, height: view.bounds.size.height)

		    // Check if license file exists
		    let licenseFile = "Orion360_SDK_Pro_iOS_Trial_fi.finwe.OrionPro-VideoPlayer.lic"
		    let path: String? = Bundle.main.path(forResource: licenseFile, ofType: nil)
		    var isDir: ObjCBool = false
		    let fileManager = FileManager.default

		    if fileManager.fileExists(atPath: path!, isDirectory:&isDir)
		    {
			let licenseUrl = URL(fileURLWithPath: path ?? "")
			//If license file found, assign it to orionView's licenceFileUrll
			orionView.licenseFileUrl = licenseUrl
		    }
		    else {
			print("No license file found.")
		    }

		    self.view.addSubview(orionView)
		    orionView.overrideSilentSwitch = true
		    orionView.alpha = 0.0

		    //Create an instance of OrionVideoContent
		    videoContent = OrionVideoContent()
		    videoContent.delegate = self

		    let videoUrl = URL(string: "https://player.vimeo.com/external/187645100.m3u8?s=2fb48fc8005cebe2f10255fdc2fa1ed6da59ea53")
		    videoContent.uriArray = [videoUrl!]
		    orionView.add(videoContent)

		    viewPort = OrionViewport(frame: CGRect(x: 0, y: 0, width: view.bounds.size.width, height: view.bounds.size.height), lockInPosition: false)
		    viewPort.viewportConfig.fullScreenEnabled = true
		    orionView.add(viewPort, orionContent: videoContent)

		}

	    }

	    func orionVideoContentReady(toPlayVideo orionVideoContent: OrionVideoContent) {

		UIView.animate(withDuration: 0.2, animations: {(_: Void) -> Void in
		    self.orionView.alpha = 1.0
		}, completion: {(_ finished: Bool) -> Void in
		    orionVideoContent.play(0.0)
		})
		print("OrionVideoContentReady")

	    }

	    func orionVideoContentDidReachEnd(_ orionVideoContent: OrionVideoContent) {
		orionVideoContent.seek(to: 0.0)
	    }


	}

Note: If you are using images/video from URL, make sure your sources are from HTTPS. Apple’s ATS Policy,  App Transport Security start blocking a cleartext HTTP (http://) resource load since it is insecure. Temporary exceptions can be configured via your app's Info.plist file.


## Run OrionPro-VideoPlayer 

The Scheme pop-up menu lets you choose which simulator or device you’d like to run your app on. On Figure 26 iPhone 8 Plus Simulator is selected.

![screen shot 2018-03-14 at 15 20 36](https://user-images.githubusercontent.com/36510685/37404876-c7ab783a-279b-11e8-8559-3fec73585ebe.png)

Figure 26. Xcode’s toolbar

Save the changes and click the Run button <img width="20" alt="screen shot 2018-02-27 at 14 45 45" src="https://user-images.githubusercontent.com/36510685/37404973-0dc01a88-279c-11e8-9d58-045faf934d61.png"> or press ![screen shot 2018-02-27 at 16 23 48](https://user-images.githubusercontent.com/36510685/37404980-123a2ee6-279c-11e8-936c-0ec85a947b12.png) to build and run OrionPro_VideoPlayer and you are able to see a video in true 360° experience. Feel free to zoom, pan and swipe. 

Completed version of OrionPro_Player can be downloaded [here](https://github.com/FinweLtd/orion360-sdk-pro-hello-ios.git).


## Next Steps


It is recommended to get familiar with the [wiki](https://github.com/FinweLtd/OrionSDK_iOS_Prd/wiki) pages and API documentation that is included in the SDK to learn more about the available features and how they should be used.

Take a look at the delivered sample apps to get more familier with our SDK. Sample projects are done using Objective-C and Swift. 
Objective-C: [https://github.com/FinweLtd/orion360-sdk-pro-examples-ios](https://github.com/FinweLtd/orion360-sdk-pro-examples-ios), 
Swift: 

Clone the projects and follow steps mentioned in [Getting started with Podfile](#getting-started-with-podfile). 

Open .xcworkspace, build and run and project. Then look at the source code.

## Feedback and Support


Feedback & support should be directed via email to support@finwe.fi .
