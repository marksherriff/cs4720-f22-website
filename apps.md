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
{: .no_toc }

First, head to GitHub to create your repo in our classroom GitHub organization by going here: [https://classroom.github.com/a/Hdx06N37](https://classroom.github.com/a/Hdx06N37).  

Please name your project your UVA computing ID!

Once you have created your repo, you should have a url that looks something like this: https://github.com/uva-cs4720-f22/android-mss2x.git

Android Studio has GitHub integration built in, but making a project connect to a repo that's NOT in your personal account is slightly trickier in the UI.  Please do the following steps:

1. Clone your repository on GitHub for the project to your machine to wherever you want to work on the project.  This repo will automatically have a README file (that you should edit!) and a .gitignore (which you should _not_ edit!).
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

For your Android Mini App, you are going to build a simple UVa Bucket List app.  Users will be able to open this app and add items to their bucket list of things that they want to do before graduation.  Each item will have a name, description, latitude, longitude, and a way to record whether it has been completed or not.  Since we are early in the semester and have not yet covered data storage, the app should pre-populate with just a few example items at start up and work as intended while in use, but it does not have to remember the state of the list from run to run.

### Requirements and Specifications

Your app must meet the following requirements.  Beyond these requirements, you can customize your app as you see fit.

The app must have these three activity screens - a list screen, a create new item screen, and an item information screen.  More detailed information about each activity is found below.

__List Activity__

1. When the app starts up, the list screen should be the first one displayed.
2. I suggest using a `RecyclerView` as seen [in this Android course](https://developer.android.com/courses/pathways/android-basics-kotlin-unit-2-pathway-3).
3. Each bucket list item must list: the name of the item, the due date, and a checkbox (or something similar) for a user to click to check off the item as being done.
4. There must be a button somewhere on the screen (usuall a floating circular button in the lower right) to go to the add item activity.
5. The items in the list should be in order from soonest due date to latest.
6. Tapping on any item (not on the checkbox) should bring up an Edit Item activity (see that Activity for more info).
7. Tapping on the checkbox next to an item should flip it's done / not done status.
8. Tapping on the floating action button should bring up the Add Item activity (see that Activity for more info).  To launch this activity, you should use the `startActivityForResult()` method.  Upon completion of the Add Item activity, you should use `onActivityResult(int requestCode, int resultCode, Intent data)` to parse the result and add the new item to the `ArrayList` in this activity.

__Add Item Activity__

1. The screen should have a back arrow in the upper left corner, which cancels the add.  This could be done using a custom Toolbar.
2. The screen should have fields for each of the parts of a bucket list item, along with a DatePicker for the due date.
3. There should be a save button at the bottom of the screen.
4. The activity should send the info from the fields back as extra data fields in the return intent.

__Item Info Activity__

1. The screen should look the same as the Add Item activity, but with the information pre-populated with the information from the item you tapped.
2. Any changes made here should be reflected back in the original item.
3. If the due date changes, you should re-sort the the list.

__BucketItem__

1. You will need some sort of data class for holding the bucket list items.  
2. The item needs to contain: name of the item, due date, whether it has been completed or not (boolean).

### Submission and Grading

__Submission__

For the app itself, you do not need to do any manual submission.  We will grade the latest version in your GitHub repo.  

For the report described below, please submit the required information into the associated assignment in Gradescope.

20 XP: App can launch properly and a screen with a pre-populated, sorted list appears    
10 XP: Tapping on the floating action button launches the Add New Item activity       
20 XP: A new item is put into the list in the correct location after saving    
10 XP: Tapping on the check box registers the item as complete and it moves to the bottom of the list    
10 XP: Tapping on the name of an item opens the Edit Item activity    
10 XP: The Edit Item activity is pre-populated with all appropriate data   
20 XP: Changes made in the Edit Item activity are properly reflected back in the list   
10 XP: The back arrows in the upper left corner work properly for both Add New Item and Edit Item   
10 XP: App does not crash on rotate (fully resetting the entire app on rotate: -5 XP)   
20 XP: Design / Style / Appearance / Usability   
10 XP: Documentation / Report 

__Project Report__

Please answer the questions on the _Android UVA Bucket List_ assignment in Gradescope _and_ put this information into your README file in GitHub:

* Your name and UVA computing ID
* Any special features about your app we should know about
* Lessons learned from building this Android app (a paragraph at least)



## UVA Bucket List (iOS)

## UVA Bucket List (React Native)





## Final Project