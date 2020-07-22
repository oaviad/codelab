author: Oren Aviad
summary: A Deep Dive into Espresso
id: docs
categories: codelab,markdown
environments: Web
status: Published
feedback link: A link where users can go to provide feedback (Maybe the git repo)
analytics account: Google Analytics ID

# How to Write Automation Tests with Espresso

## Overview

This tutorial shows you how to write automation tests with Espresso: Android automated testing framework.

### What You’ll Learn 
- How to setup Espress
- How to record Espresso Test, Save it & Run
- How to write Espreso Tests

### Prerequisites 
* Android Studio
* Android Device
* Source Control Tool: GitExtensions/Sourcetree

## What is the Espresso Framework?

Positive
: The Espresso testing framework provides a set of APIs to build UI tests to test user flows within an app. These APIs let you write automated UI tests that are concise and that run reliably. Espresso is well-suited for writing white box-style automated tests, where the test code utilizes implementation code details from the app under test.

The main components of Espresso:
* Espresso: Entry point to interactions with views (via onView() and onData()). Also exposes APIs that are not necessarily tied to any view, such as pressBack().
* ViewMatchers:  allows you to find a view in the current view hierarchy.
* ViewActions: allows you to perform actions on the views.
* ViewAssertions: allows you to assert the view state.

## App Overview

In this tutorial you will modify the [EspressoClub](https://github.com/oaviad/espressoClub) project. You will setup Espresso in the project for testing and then you will test the app's functionality.

See figures below. 

![tomtom_portal](assets/login_activity.png) 
![tomtom_portal](assets/main_activity.png)

## Espresso Setup Instructions

### Add Espresso dependencies

In your app's top-level build.gradle file, you need to specify these libraries as dependencies:

``` gradle

dependencies {
    androidTestImplementation 'androidx.test:core-ktx:1.2.0'
    androidTestImplementation 'androidx.test.ext:junit-ktx:1.1.1'
    androidTestImplementation 'androidx.test:runner:1.2.0'
    androidTestImplementation 'androidx.test:rules:1.2.0'
    androidTestImplementation 'androidx.test.espresso:espresso-core:3.2.0'
    androidTestImplementation 'androidx.test.espresso:espresso-intents:3.2.0'
    androidTestImplementation "com.google.truth:truth:0.44"
}
```

### Set the instrumentation runner

``` gradle
testInstrumentationRunner "androidx.test.runner.AndroidJUnitRunner"
```

In your app's top-level build.gradle file, you need to specify these libraries as dependencies:

## Espresso Test Recorder

Positive
: The Espresso Test Recorder tool lets you create UI tests for your app without writing test code. By recording a test scenario, you can record your interactions with a device and add assertions to verify UI elements in particular snapshots of your app. Espresso Test Recorder then takes the saved recording and automatically generates a corresponding UI test that you 
can run to test your app

To start recording a test with Espresso Test Recorder:

* Click Run > Record Espresso Test.

* In the Select Deployment Target window, choose the device on which you want to record the test. Click OK.

* Espresso Test Recorder triggers a build of your project, and the app must install and launch before Espresso Test Recorder allows you to interact with it. The Record Your Test window appears after the app launches. Interact with your device to start logging events such as "tap" and "type" actions.

* To save a recording, click OK.

## Task1: Record login flow

## Task2: Validate user enters valid credentials

## Task3: Validate user enters invalid credentials

## Task4: Validate login button is sending the right Intent

## Task5: Setup Intent before launching Activity

## Summary

