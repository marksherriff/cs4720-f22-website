---
layout: default
title: Mobile Apps
nav_order: 4
---

# Mobile App Assignments
{: .no_toc }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## UVA Bucket List (Android)

### Getting Started: GitHub and Android Studio

First, head to GitHub to create your repo in our classroom GitHub organization by going here: [https://classroom.github.com/a/Hdx06N37](https://classroom.github.com/a/Hdx06N37).  

Please name your project your UVA computing ID!

Once you have created your repo, you should have a url that looks something like this: https://github.com/uva-cs4720-f22/android-mss2x.git

Android Studio has GitHub integration built in, but making a project connect to a repo that's NOT in your personal account is slightly trickier in the UI.  Please do the following steps:

1. Clone your repository on GitHub for the project to your machine to wherever you want to work on the project.  This repo will automatically have a `README` file (that you should edit!) and a `.gitignore` (which you should _not_ edit!).
2. Open Android Studio and create a New Project.
3. Select "Phone and Tablet" on the left and choose "Empty Activity."
4. For the Application Name, please call it just your computing ID.  (Yes, I know this isn't going to look great, but if we have 90 "UVA Bucket List" named apps on our phones when we grade, it just makes it harder!  You can change this later if you want to.)
5. The package name should be "edu.virginia.cs4720.bucketlist.mss2x" where "mss2x" is your computing ID.
6. For the Save Location, choose the directory you just cloned from GitHub.  Ignore the warning that it already exists and is not empty.
6. Keep the language as Kotlin and the minimum SDK at API 21: Android 5.0 (Lollipop).
7. In the bottom right, you may get a popup asking about adding project configuration files to Git.  Choose "Always Add."
8. Now let's commit and push this starter project to GitHub.  Choose Git->Commit from the top menu.
9. Check the box beside "Unversioned Files" so that it will add all files in the project to this commit.
10. Add a commit message in the box below and then click "Commit and Push..."  You will probably have some warnings, etc.  Click "Commit Anyway and Push..." if it appears.  Then click "Push" again.  (Yes, there are a lot of steps this first time...)
11. Your project will not be in GitHub!  You can continue to use Android Studio for committing/pushing your code or you can use the git tool of your choice.
12. REMEMBER: your final submission will be whatever is in GitHub at the time the project is due!

### Requirements and Specifications

For your Android Mini App, you are going to build a simple UVA Bucket List app.  Users will be able to open this app and add items to their bucket list of things that they want to do before graduation.  Each item will have a name, a due date, and a way to record whether it has been completed or not.  The app should pre-populate with just a few example items at start up and work as intended while in use, but it does not have to remember the state of the list from run to run.  (In other words, you are not required to implement permanent storage with a database, cloud service, or other file writing.)

Your app must meet the following requirements.  Beyond these requirements, you can customize your app as you see fit.

The app must have these three activity screens - a list screen, a create new item screen, and an item information screen.  More detailed information about each activity is found below.

__List Activity__

1. When the app starts up, the list screen should be the first one displayed.
2. I suggest using a `RecyclerView` as seen [in this Android course](https://developer.android.com/courses/pathways/android-basics-kotlin-unit-2-pathway-3).
3. Each bucket list item must list: the name of the item, the due date, and a checkbox (or something similar) for a user to click to check off the item as being done.
4. There must be a button somewhere on the screen (usually a floating circular button in the lower right) to go to the add item activity.
5. The items in the list should be in order from soonest due date to latest.
6. Tapping on any item (not on the checkbox) should bring up an Edit Item activity (see that Activity for more info).
7. Tapping on the checkbox next to an item should flip it's done / not done status.
8. Tapping on the floating action button should bring up the Add Item activity (see that Activity for more info).  

__Add Item Activity__

1. The screen should have a back arrow in the upper left corner, which cancels the add.  This could be done using a custom Toolbar.
2. The screen should have fields for each of the parts of a bucket list item, along with a DatePicker for the due date.
3. There should be a save button at the bottom of the screen.
4. The activity should send the info from the fields back as extra data fields in the return intent.

__Item Info Activity__

1. The screen should look the same as the Add Item activity, but with the information pre-populated with the information from the item you tapped AND it should also have the date that the item was completed.
2. Any changes made here should be reflected back in the original item.
3. If the due date changes, you should re-sort the the list.

__BucketItem__

1. You will need some sort of data class for holding the bucket list items.  
2. The item needs to contain: name of the item, due date, whether it has been completed or not (boolean), and the date that it was completed.

### Submission and Grading

__Submission__

For the app itself, you do not need to do any manual submission.  We will grade the latest version in your GitHub repo.  

For the report described below, please submit the required information into the associated assignment in Gradescope.

* 20 XP: App can launch properly and a screen with a pre-populated, sorted list appears (sorted by soonest due at the top, then all completed items at the very bottom, sorted by date completed)   
* 10 XP: Tapping on the floating action button launches the Add New Item activity       
* 20 XP: A new item is put into the list in the correct location after saving    
* 10 XP: Tapping on the check box registers the item as complete and it moves to the bottom of the list    
* 10 XP: Tapping on the name of an item opens the Edit Item activity    
* 10 XP: The Edit Item activity is pre-populated with all appropriate data   
* 20 XP: Changes made in the Edit Item activity are properly reflected back in the list   
* 10 XP: The back arrows in the upper left corner work properly for both Add New Item and Edit Item   
* 10 XP: App does not crash on rotate (fully resetting the entire app on rotate: -5 XP)   
* 20 XP: Design / Style / Appearance / Usability   
* 10 XP: Documentation / Report 

__Project Report__

Please answer the questions on the _Android UVA Bucket List_ assignment in Gradescope _and_ put this information into your `README` file in GitHub:

* Your name and UVA computing ID
* Any special features about your app we should know about
* Lessons learned from building this Android app (a paragraph at least)

__Late Policy__

Changes made to the GitHub repo after the due date and time will incur the following penalties:
* -15 XP up to 1 day late
* -30 XP up to 2 days late
* -60 XP up to 3 days late
* -120 XP up to 4 days late

### Tips
{: .no_toc }

1. Note that a "Bucket List" is _super similar_ to a to-do list.  Consider that when you are looking for tutorials.
2. If you use code from elsewhere, it MUST be cited.  Also, wholesale using the "solution" from a tutorial you find that's "close enough" in your opinion is not going to earn any XP.

## UVA Bucket List (React Native)

### Getting Started: GitHub and Development Environment

First, head to GitHub to create your repo in our classroom GitHub organization by going here: [https://classroom.github.com/a/9cJRPiZX](https://classroom.github.com/a/9cJRPiZX).  

Please name your project your UVA computing ID!

Once you have created your repo, you should have a url that looks something like this: https://github.com/uva-cs4720-f22/reactnative-mss2x.git

It seems that most everyone is using VS Code at this point as their editor of choice.  I would suggest not using Android Studio at least because I've seen students open just the Android directory (where the gradle project is) and not be able to work with the JS.  I would also suggest doing most of your terminal work in an actual terminal and not the embedded one inside VS Code, but it's up to you.  Regardless of what code editor you decide to use, I suggest the following steps for getting set up with your GitHub repo.  I had some initial problems getting the project to connect to the proper repo because 1) GitHub Classroom generates repo names with a hyphen in them, and b) React Native projects can't have a hypen in their name.  :shrug:

1. Accept the GitHub Classroom assignment as explained above.
2. Navigate to the folder on your computer where you want to create the project folder.
3. Create your project with the command `npx react-native init reactnative_XXXXXXX`, replacing `XXXXXXX` with your own ID.
4. Change directory into the project directory and connect your project to the GitHub repo with the following commands (editing as necessary):

```
git init
git add *
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:uva-cs4720-f22/reactnative-XXXXXXX.git
git push -u origin main
```

Everything should be connected properly now.  Remember: if you clone the repo to somewhere new, you'll probably need to re-install all of the modules you use with `npm`.

If you wish to use `expo` to create your app from scratch, that's fine.  Replace the appropriate project creation command above, but the GitHub connection should be the same.

### Requirements and Specifications

For your React Native Mini App, you are going to build a simple UVA Bucket List app.  Users will be able to open this app and add items to their bucket list of things that they want to do before graduation.  Each item will have a name, a due date, and a way to record whether it has been completed or not.  The app should pre-populate with just a few example items at start up and work as intended while in use, but it does not have to remember the state of the list from run to run.  (In other words, you are not required to implement permanent storage with a database, cloud service, or other file writing.)

Your app must meet the following requirements.  Beyond these requirements, you can customize your app as you see fit.

You are allowed to build a plain React Native app, build the app using Expo, or a React Native app that imports certain Expo libraries.

The app must have these three screens - a list screen, a create new item screen, and an item information screen.  More detailed information about each screen and other needed files is found below.

__App.js__

1. Remember that `App.js` is the first file that is executed, and you should probably have a `NavigationContainer` here, as seen in [https://github.com/uva-cs4720-f22/MyDailySchedule/blob/main/App.js](https://github.com/uva-cs4720-f22/MyDailySchedule/blob/main/App.js).
2. I suggest creating a different JS file for each screen, placing them in an apprpriately named folder.

__List Screen__

1. When the app starts up, the list screen should be the first one displayed. 
2. I suggest using a `ScrollView` as seen in the `AwesomeProject` example app.
3. Each bucket list item must list: the name of the item, the due date, and a checkbox (or something similar) for a user to click to check off the item as being done.
4. There must be a button somewhere on the screen to go to the add item screen.  You can do this however you see fit.
5. The items in the list should be in order from soonest due date to latest.
6. Tapping on any item (not on the checkbox) should bring up an Edit Item screen (see that screen for more info).
7. Tapping on the checkbox next to an item should flip it's done / not done status.
8. Tapping on the floating action button should bring up the Add Item screen (see that screen for more info).  

__Add Item Screen__

1. The screen should have a back arrow in the upper left corner, which cancels the add.  You should get this automatically using the `NavigationContainer.`
2. The screen should have fields for each of the parts of a bucket list item, along with a date picker for the due date.
3. There should be a save button at the bottom of the screen.
4. The screen should send the info from the fields back as extra data fields in the return intent.

__Item Info Screen__

1. The screen should look the same as the Add Item screen, but with the information pre-populated with the information from the item you tapped AND it should also have the date that the item was completed.
2. This could literally be the same `.js` file as the add item screen if you choose to implement it that way.
2. Any changes made here should be reflected back in the original item.
3. If the due date changes, you should re-sort the the list.

__Bucket Item__

1. I suggest creating a `.js` file that represents the bucket list item, but it is not required.  
2. Remember that JavaScript has (of course) JSON readily available.  It is fully possible to implement the list with nested JSON objects.

### Submission and Grading

__Submission__

For the app itself, you do not need to do any manual submission.  We will grade the latest version in your GitHub repo.  

For the report described below, please submit the required information into the associated assignment in Gradescope.

* 20 XP: App can launch properly and a screen with a pre-populated, sorted list appears (sorted by soonest due at the top, then all completed items at the very bottom, sorted by date completed)   
* 10 XP: Tapping on the appropriate button launches the Add New Item screen       
* 20 XP: A new item is put into the list in the correct location after saving from the add screen   
* 10 XP: Tapping on the check box registers the item as complete and it moves to the bottom of the list    
* 10 XP: Tapping on the name of an item opens the Edit Item screen    
* 10 XP: The Edit Item screen is pre-populated with all appropriate data   
* 20 XP: Changes made in the Edit Item screen are properly reflected back in the list   
* 10 XP: The back arrows in the upper left corner work properly for both Add New Item and Edit Item   
* 10 XP: App does not crash on rotate (fully resetting the entire app on rotate: -5 XP)   
* 20 XP: Design / Style / Appearance / Usability   
* 10 XP: Documentation / Report 

__Project Report__

Please answer the questions on the _React Native UVA Bucket List_ assignment in Gradescope _and_ put this information into your `README` file in GitHub:

* Your name and UVA computing ID
* Any special features about your app we should know about
* Lessons learned from building this React Native app (a paragraph at least)

__Late Policy__

Changes made to the GitHub repo after the due date and time will incur the following penalties:
* -15 XP up to 1 day late
* -30 XP up to 2 days late
* -60 XP up to 3 days late
* -120 XP up to 4 days late

### Tips
{: .no_toc }

1. Note that a "Bucket List" is _super similar_ to a to-do list.  Consider that when you are looking for tutorials.
2. If you use code from elsewhere, it MUST be cited.  Also, wholesale using the "solution" from a tutorial you find that's "close enough" in your opinion is not going to earn any XP.

## UVA Bucket List (iOS)

### Getting Started: GitHub and Development Environment

First, head to GitHub to create your repo in our classroom GitHub organization by going here: [https://classroom.github.com/a/Wk1Pmvpd](https://classroom.github.com/a/Wk1Pmvpd).  

Please name your project your UVA computing ID!

Once you have created your repo, you should have a url that looks something like this: https://github.com/uva-cs4720-f22/ios-mss2x.git

1. Clone the repository locally to your machine.
2. Open Xcode and create a new iOS App.
3. For the Product Name, call it `Bucket List COMPID`, replacing `COMPID` for your computing ID.
4. Select whether you want to do Storyboard or SwiftUI.
5. When prompted for where you want to save the project, select the folder you just cloned from GitHub.
6. First thing you should do is click Source Control in the top menu and Commit.
7. Add a comment at the bottom of the window and hit the check box in the lower left to Push to remote.  
8. Commit and Push in the lower right.  That should get you ready to start working.

### Requirements and Specifications

For your iOS Mini App, you are going to build a simple UVA Bucket List app.  Users will be able to open this app and add items to their bucket list of things that they want to do before graduation.  Each item will have a name, a due date, and a way to record whether it has been completed or not.  The app should pre-populate with just a few example items at start up and work as intended while in use, but it does not have to remember the state of the list from run to run.  (In other words, you are not required to implement permanent storage with a database, cloud service, or other file writing.)

Your app must meet the following requirements.  Beyond these requirements, you can customize your app as you see fit.

You are allowed to build your app using either Storyboards or SwiftUI.  However, I have done almost nothing with SwiftUI and thus my suggested files and instructions below are going to be for Storyboards.

The app shall be made up of four total screens - the launch screen, a list screen, a create new item screen, and an item information screen.  More detailed information about each scene is found below.

You will (most likely) have some set of the following files in your project:

* `AppDelegate.swift` - Basically the "main" for the entire app.  You probably won't touch this.
* `AddItemViewController.swift` - The Add New Item controller code.
* `EditItemViewController.swift` - The Edit Item controller code.
* `Main.storyboard` - The storyboard for most of your app (not count the launch screen).
* `LaunchScreen.storyboard` - Built-in by default, you just need to add your names to this.
* `BucketItem.swift` - The model class for this app.
* `BucketListTableViewController.swfit` - The controller for the list screen.
* `BucketListTableViewCell.swift` - Effectively the adapter for this app if you think of the Android version.

__BucketListTableViewController, BucketListTableViewCell, and BucketItem__

A very large portion of your overall code base will go here. There are a LOT of tutorials out there on how to do this.  PLEASE read through several to get a feel for all of the different functions you have to override, etc.  Here is a sampling:

* [Swift Language Reference](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/TheBasics.html)
* [Apple's Tutorial](https://developer.apple.com/library/content/referencelibrary/GettingStarted/DevelopiOSAppsSwift/)
* [raywenderlich.com](https://www.raywenderlich.com/category/ios)
* [iOS Cookbook Examples](https://github.com/vandadnp/iOS-8-Swift-Programming-Cookbook/tree/master/chapter-tables)
* [Ralf Ebert](https://www.ralfebert.de/tutorials/ios-swift-uitableviewcontroller/)
* [Making App Pie](https://makeapppie.com/2016/10/03/introducing-table-views-in-swift-3/)

Also please check the lecture notes for example code on how to do a list like this!

The requirements are basically the same as the other versions:

1. The list should be sorted first by whether the item still needs to be done or not (completed items move to the bottom), then by date (with more recent dates at the top).  (This is the same as the others.)
2. I found that including an element to allow for swiping right to left should show a button to mark the item done and to edit the item actualy is easier to do in iOS than trying to have an actual checkbox or tapping on the item.  Here is an example project I made that has the slide element: [https://github.com/marksherriff/NoteTaker-iOS](https://github.com/marksherriff/NoteTaker-iOS)
3. The button should swap the done / not done state, and also change the background color of the cell to show its state (this is in lieu of having an actual checkbox).
4. Tapping on the + in the upper right takes you to the add new screen.


__Add Item and Edit Item__

1. You should have Cancel and Save buttons along the top in a `Navigation Controller`.
2. Make sure that the numeric fields are numeric entry and that the date is a date-only spinner.
3. Added or edited items should appear in the list upon save and the order fixed if needed.
4. It is possible to use only one scene to do both add and edit.  If you want to do this, you are welcome to do so, but note that it can be a bit more complicated (if overall it is less code).

Moving between scenes and passing data requires the use of segues.  Examples:

* [Apple's Tutorial](https://developer.apple.com/library/content/featuredarticles/ViewControllerPGforiPhoneOS/UsingSegues.html)
* [raywenderlich.com](https://www.raywenderlich.com/113394/storyboards-tutorial-in-ios-9-part-2)
* [Coding Explorer](http://www.codingexplorer.com/segue-swift-view-controllers/)


__Storyboards__

Layout management can be interesting in Swift and Xcode.  Again, here are some resources:

* [Apple's Tutorial](https://developer.apple.com/library/content/documentation/UserExperience/Conceptual/AutolayoutPG/index.html#//apple_ref/doc/uid/TP40010853-CH7-SW1)
* [raywenderlich.com](https://www.raywenderlich.com/113388/storyboards-tutorial-in-ios-9-part-1)

### Submission and Grading

__Submission__

For the app itself, you do not need to do any manual submission.  We will grade the latest version in your GitHub repo.  

For the report described below, please submit the required information into the associated assignment in Gradescope.

* 20 XP: App can launch properly and a screen with a pre-populated, sorted list appears (sorted by soonest due at the top, then all completed items at the very bottom, sorted by date completed)   
* 10 XP: Tapping on the appropriate button launches the Add New Item screen       
* 20 XP: A new item is put into the list in the correct location after saving from the add screen   
* 10 XP: Tapping some appropriate element registers the item as complete and it moves to the bottom of the list    
* 10 XP: Tapping some appropriate element opens the Edit Item screen    
* 10 XP: The Edit Item screen is pre-populated with all appropriate data   
* 20 XP: Changes made in the Edit Item screen are properly reflected back in the list   
* 10 XP: The Cancel in the upper left corner work properly for both Add New Item and Edit Item   
* 10 XP: App does not crash on rotate (fully resetting the entire app on rotate: -5 XP)   
* 20 XP: Design / Style / Appearance / Usability   
* 10 XP: Documentation / Report 

__Project Report__

Please answer the questions on the _React Native UVA Bucket List_ assignment in Gradescope _and_ put this information into your `README` file in GitHub:

* Your name and UVA computing ID
* Any special features about your app we should know about
* Lessons learned from building this React Native app (a paragraph at least)

__Late Policy__

Changes made to the GitHub repo after the due date and time will incur the following penalties:
* -15 XP up to 1 day late
* -30 XP up to 2 days late
* -60 XP up to 3 days late
* -120 XP up to 4 days late

### Tips
{: .no_toc }

1. Note that a "Bucket List" is _super similar_ to a to-do list.  Consider that when you are looking for tutorials.
2. If you use code from elsewhere, it MUST be cited.  Also, wholesale using the "solution" from a tutorial you find that's "close enough" in your opinion is not going to earn any XP.


## Final Project