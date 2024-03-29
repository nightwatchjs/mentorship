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
__Discord Community:__ https://discord.com/invite/SN8Da2X  
__GSoC Contributor Guidance:__ [GSoC-contributor-guidance.md](GSoC-contributor-guidance.md)

## Idea 1: Video Evidence (Video recording of tests)

### Abstract

While Nightwatch.js currently offers an integrated HTML reporter which helps aggregate and visualize the test results, along with HTML snapshots of the website state at the point of test failure, it has been a long-standing request from the community to add support for providing complete video recordings of the test runs as well, in case of test failure.

__Mentors__: Vaibhav Singh, David Burns

### Goals & Ideas

* Add the ability to record the complete test run in video format, across all major web browsers.
* Integrate the video recordings into the Nightwatch HTML Reporter.
* Add the ability to seek through the video by clicking on the test steps.
* If the tests are being run on a remote server, add the ability to download the video recording of tests from the remote server.
* Contributors are encouraged to research on all the possible ways in which test runs can be recorded in video format and discuss those solutions with the team before starting to build on them.

#### Refs

* https://nightwatchjs.org/guide/reporters/use-html-reporter.html
* https://webdriver.io/docs/wdio-video-reporter/

__Skills Required:__ JavaScript, Node.js, ReactJS (for HTML Reporter)

__Time Estimate:__ 350 hours

__Difficulty:__ Medium

## Idea 2: Add improvements to `@nightwatch/mobile-helper` tool

### Abstract

`@nightwatch/mobile-helper` is a tool that allows developers and testers to set up a fully functional Android Emulator environment in just a few minutes, without the need to download the complete Android Studio IDE software.

This tool comes in very handy while setting up Android Emulators for end-to-end web or native app testing so that the testers can go from nothing to running their first test on an Android Emulator in under 3 minutes. Additionally, this tool can also be used by other users for setting up Android Emulator environments.

__Mentors:__ Priyansh Garg

### Goals & Ideas

* Currently, the tool installs some additional requirements (ex. `chromedriver` binary) to work with Nightwatch. Add a `--standalone` option to the tool so that it only install what is required when not using with Nightwatch. This will help this tool serve a wider community.
* Find and document in one place all the important Android SDK commands that the users can use to install the system images of additional Android versions and create Android Virtual Devices (AVDs) using them, and other things like installing an application, starting/stopping the emulator, etc.
* Add the ability to allow installation of the system images of additional Android versions by letting users select from a list of available versions. Currently, the tool can only install the system image of Android version 11.
* Add the ability to create multiple Android Virtual Devices (AVDs) which can be used to emulate a wider range of Android Devices like Pixel 6, Pixel XL, etc. Currently, the tool can only create an AVD for Pixel 5 device.
* Add the ability to allow users to update the various Android SDK tools required to run Android Emulator, by giving them a list of all the tools that can be updated (along with their current version and latest versions), and an option to update all the SDK tools in one go.
* Add the ability to connect Android devices to `adb` wirelessly by running command `npx @nightwatch/mobile-helper android --connect --wireless`, which would allow users to automate Android devices wirelessly: https://developer.android.com/tools/adb#wireless-android11-command-line

#### Refs

* https://github.com/nightwatchjs/mobile-helper-tool
* https://developer.android.com/tools

__Skills Required:__ TypeScript, Node.js, Android SDKs

__Time Estimate:__ 350 hours

__Difficulty:__ Medium

## Idea 3: Integrate WebDriver BiDi in Nightwatch.js

### Abstract

Currently, Nightwatch.js and other Selenium-based end-to-end testing tools depend on [W3C Webdriver API](https://www.w3.org/TR/webdriver/) specifications for automating web browsers, which being a standardized API works great, but it still has a few limitations arising from its traditional HTTP based request/response architecture, which makes it slower and unable to make use of the full potential of event-driven nature of web browsers.

Enter [WebDriver BiDi](https://w3c.github.io/webdriver-bidi/), which is a new standard protocol for browser automation currently under active development, which makes use of the event-based WebSocket connections instead of the traditional HTTP connections, making full use of the event-driven nature of web browsers to provide many additional functionalities (like network interception, observing DOM mutation, listening to JS exceptions, etc.) over and above the existing WebDriver APIs while making them much faster.

__Mentors__: Puja Jagani, Ravi Sawlani, David Burns

### Goals & Ideas

* Make the required changes in Nightwatch.js so that it can work with the new WebDriver BiDi protocol alongside the WebDriver API protocol.
* Migrate the existing [CDP (Chrome Devtools Protocol)](https://chromedevtools.github.io/devtools-protocol/) based commands to use the new browser-agnostic WebDriver BiDi Protocol, which will make those commands work on non-Chromium based browsers as well.
* Implement new functionalities using WebDriver BiDi Protocol like [Script Pinning](https://www.selenium.dev/documentation/webdriver/bidirectional/chrome_devtools/bidi_api/#pin-scripts), [DOM Mutation Observer](https://www.selenium.dev/documentation/webdriver/bidirectional/chrome_devtools/bidi_api/#mutation-observation), etc.
* Make sure the existing Nightwatch.js APIs continue to work as expected after transitioning to WebDriver BiDi protocol, and in case of any discrepancies, report the same to the [Selenium](https://github.com/SeleniumHQ/selenium) project.
* Update API documentations accordingly.

#### Refs

* https://developer.chrome.com/docs/web-platform/best-practices/webdriver-bidi
* https://www.selenium.dev/documentation/webdriver/bidirectional/
* https://www.selenium.dev/documentation/webdriver/bidirectional/chrome_devtools/bidi_api/#mutation-observation

__Skills Required:__ JavaScript, Node.js, Selenium, WebSockets

__Time Estimate:__ 350 hours

__Difficulty:__ Medium

## Idea 4: Improve Nightwatch v3 Element API

### Abstract

With the v3 release last year, Nightwatch.js introduced a brand new Element API which provides a much more concise way of finding and interacting with elements. And while this was a major step towards improving the test writing experience for Nightwatch.js users, there are still a few areas where this experience can be improved further.

Additionally, we also need to get better at promoting this new and better element API by updating our existing example tests and writing new tests that clearly shows the benefits we get from using the new API.

__Mentors:__ Andrei Rusu, Priyansh Garg

### Goals & Ideas

* Add a few missing capabilities (commands) to Nightwatch v3 Element API: https://github.com/nightwatchjs/nightwatch/issues/3901
* Make action commands on the new Element API chainable, which will further improve the test writing experience for users. For example, we should be able to chain `.click()` and `.sendKeys()` command as: `browser.element.find().click().sendKeys()`.
* Make sure that the action commands throw error incase an error is returned by Selenium: https://github.com/nightwatchjs/nightwatch/issues/3899
* Add a `force` parameter on the `.click()` command to force click on an element incase the normal click does not work.
* Add improvements to Testing Library `.findByRole()` command: https://github.com/nightwatchjs/nightwatch/issues/3887
* Update Nightwatch [example tests](https://github.com/nightwatchjs/nightwatch/tree/main/examples) to use the new Element API syntax.
* Add new example tests that shows the usage of all the commands/assertions available with the new Element API. This will not only serve as a direct reference for the users to check how to use a command, but will also serve as a regression test suite for Nightwatch.js that we can run regularly to make sure we are not breaking anything in subsequent releases.

#### Refs

* https://nightwatchjs.org/api/element/

__Skills Required:__ JavaScript/TypeScript, Node.js

__Time Estimate:__ 350 hours

__Difficulty:__ Easy/Medium
