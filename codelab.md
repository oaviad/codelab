author: Oren Aviad
summary: How to Write Automation Tests with Espresso
id: docs
categories: codelab,markdown
environments: Web
status: Published
feedback link: A link where users can go to provide feedback (Maybe the git repo)
analytics account: Google Analytics ID

# How to Write Automation Tests with Espresso

## Welcome

In this codelab you will learn how to write automation tests with Espresso: Android automated testing framework.

### What You’ll Learn 
- How to setup Espresso
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
* <strong>Espresso</strong>: Entry point to interactions with views (via onView() and onData()). Also exposes APIs that are not necessarily tied to any view, such as pressBack().
* <strong>ViewMatchers</strong>:  allows you to find a view in the current view hierarchy.
* <strong>ViewActions</strong>: allows you to perform actions on the views.
* <strong>ViewAssertions</strong>: allows you to assert the view state.

Positive
: <strong>Tip</strong>: Download the [Espresso cheat sheet](https://developer.android.com/training/testing/espresso/cheat-sheet) 

## App Overview

In this codelab you will modify the [EspressoClub](https://github.com/oaviad/espressoClub) project. 
You will setup Espresso and test app's functionality.

In order to login, user has to enter valid credentials in the login screen (LoginActivity) : valid email and valid password (>5 characters).
After user has logged in, the main screen will be launched (MainActivity).

See figures below. 

![](assets/login_activity.png) 

![](assets/main_activity.png)

## Getting Started

To get the sample app:

Clone the repository from GitHub and switch to the <strong>starter</strong> branch.

``` bash
$  git clone https://oaviad.github.io/codelab
```

## Task 1: setup Espresso

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
Positive
: <strong>Tip</strong>: To learn more about <strong>Espresso Setup Instructions</strong>, you can read [here](https://developer.android.com/training/testing/espresso/setup). 

## Task 2: record login flow

To start recording a test with Espresso Test Recorder:

* Click Run > Record Espresso Test.

* In the Select Deployment Target window, choose the device on which you want to record the test. Click OK.

* Espresso Test Recorder triggers a build of your project, and the app must install and launch before Espresso Test Recorder allows you to interact with it. The Record Your Test window appears after the app launches. Interact with your device to start logging events such as "tap" and "type" actions.

* To save a recording: fill in Test class name & click OK.

Positive
: <strong>Tip</strong>: To learn more about <strong>Espresso Test Recorder</strong>, you can read [here](https://developer.android.com/studio/test/espresso-test-recorder). 

1. Record the login flow, make sure you add at least one Assertion.
2. Save your recording to Kotlin class.
3. Verify tests are working.


## Task 3: validate user enters valid credentials

## Task 4: validate user enters invalid credentials

## Task 5: validate login Intent

## Task 6: setup Intent before launching Activity

## Summary
