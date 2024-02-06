# GSoC 2024 Project Ideas

This list contains the high level ideas and goals for each of the potential projects we'd like to take up for GSoC 2024.
But please note that nothing listed below is set in stone, and while the overall outline of the projects would remain the same,
the internal details and goals of the projects are open to modifications based on the suggestions given by the contributors, as they
dive deeper into each of the projects under the guidance of the mentors.

## About Nightwatch.js

Nightwatch is an integrated testing framework powered by Node.js and using the [W3C Webdriver API](https://www.w3.org/TR/webdriver/).
It provides a complete testing solution and can be used for a wide range of testing needs, including:

* End-to-end testing of web applications and websites, on both desktop and mobile devices.
* Component testing in isolation (React / Vue / Storybook / Angular).
* Unit testing, Visual Regression testing, Accessibility testing, and API testing
* Native mobile app testing on Android & iOS.

## About Ideas

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
