# GSoC 2024 Project Ideas

This list contains the high level ideas and goals for each of the potential projects we'd like to take up for GSoC 2024.

But please note that nothing listed below is set in stone, and while the overall outline of the projects would remain the same,
the internal details and goals of the projects are open to modifications based on the suggestions given by the contributors, as they
dive deeper into each of the projects under the guidance of the mentors.

## About Nightwatch.js

[Nightwatch.js](https://nightwatchjs.org) is an integrated testing framework powered by Node.js and using the [W3C Webdriver API](https://www.w3.org/TR/webdriver/).
It provides a complete testing solution and can be used for a wide range of testing needs, including:

* End-to-end testing of web applications and websites, on both desktop and mobile devices.
* Component testing in isolation (React / Vue / Storybook / Angular).
* Unit testing, Visual Regression testing, Accessibility testing, and API testing
* Native mobile app testing on Android & iOS.

__GitHub Repo:__ https://github.com/nightwatchjs/nightwatch

## Idea 1: Video Evidence (Video recording of tests)

### Abstract

While Nightwatch.js currently offers an integrated HTML reporter which helps aggregate and visualize the test results, along with HTML
snapshots of the website state at the point of test failure, it has been a long-standing request from the community to add support for providing complete video recording of the tests as well, in case of test failure.

__Mentors__: Vaibhav Singh, David Burns

#### Goals & Ideas

* Add the ability to record the complete test run in video, format across all major web browsers.
* There can be multiple ways to achieve this:
  * Build a browser extension which can record screen (only browser window) during test run.
  * Write a script which can be injected into the browser to achieve the above.
  * Take screenshots before/after each action during test run and generate a video using them.  
* Integrate the video recordings into the Nightwatch HTML Reporter.
* Add the ability to seek through the video by clicking on the test steps.
* Add the ability to download videos from remote server if videos are being created on the server itself (server – device on which the tests are being run).
* Contributors are encouraged to do some research on all the potential solutions (not just limited to those stated above) for achieving this and discuss those solutions with the team before starting to build a solution.

#### Refs

* https://github.com/muaz-khan/RecordRTC
* https://github.com/webdriverio-community/wdio-video-reporter.

#### Skills Required

* JavaScript, Node.js

__Time Estimate:__ 350 hours

__Difficulty:__ Medium

## Idea 2: Add new functionalities to `@nightwatch/mobile-helper`

### Abstract

`@nightwatch/mobile-helper` is a tool that allows developers and testers to set up fully functional Android Emulator environment in just a few minutes, without the need to download the complete Android Studio IDE software.

This tool comes in very handy while setting up Android Emulators for end-to-end web or native app testing so that testers can go from nothing to running their first test on an Android Emulator in under 3 minutes. Additionally, this tool can also be used by other users for setting up Android Emulator environments.

__Mentors:__ Priyansh Garg

### Goals & Ideas

* Currently, the tool installs some additional requirements (ex. `chromedriver` binary) to work with Nightwatch. Add a `--standalone` option to the tool so that it only install what is required when not using with Nightwatch. This will help this tool serve a wider community.
* Find and document in one place all the important Android SDK commands that the users can use to install the system images of additional Android versions and create Android Virtual Devices (AVDs) using them, and other things like installing an application, starting/stopping the emulator, etc.
* Add the ability to allow installation of the system images of additional Android versions by letting users select from a list of available versions. Currently, the tool can only install the system image of Android version 11.
* Add the ability to create multiple Android Virtual Devices (AVDs) which can be used to emulate a wider range of Android Devices like Pixel 6, Pixel XL, etc. Currently, the tool can only create an AVD for Pixel 5 device.
* Add the ability to allow users update Android SDK binaries using the tool itself, by giving them a list of binaries that can be updated (along with the current version and latest version of the binaries), and an option to update all the binaries in one go.
* Add the ability to connect Android devices to `adb` wirelessly by running command `npx @nightwatch/mobile-helper android --connect --wireless`, which would allow users to automate Android devices wirelessly: https://developer.android.com/tools/adb#wireless-android11-command-line

#### Refs

* https://github.com/nightwatchjs/mobile-helper-tool
* https://github.com/webdriverio-community/wdio-video-reporter.

#### Skills Required

* JavaScript, Node.js, Android SDKs

__Time Estimate:__ 350 hours

__Difficulty:__ Medium
