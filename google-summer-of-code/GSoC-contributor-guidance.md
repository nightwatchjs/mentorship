# Contributor Guidance for GSoC 2024

## General guidelines

* Read the [Contributor Guide](https://google.github.io/gsocguides/student/) written by the Google Summer of Code organizers.
* Go through the [GSoC 2024 Project Ideas List](GSoC-2024-Ideas.md) for Nightwatch.js and read our [Contributing Guide](https://github.com/nightwatchjs/nightwatch/blob/main/CONTRIBUTING.md).
* Understand the [GSoC timeline](https://developers.google.com/open-source/gsoc/timeline), application process and the project you are applying for, assuming best intentions throughout the period.
* Join our [Discord server](https://discord.com/invite/SN8Da2X) and introduce yourself in the `#welcome` channel.
* Ask for any development-related help in the `#development-team` channel and direct all your GSoC related queries to the `#gsoc` channel on Discord.
* Start as early as possible and try to submit at least a few good code contributions to any project of your liking in the [Nighwatch.js GitHub Org](https://github.com/nightwatchjs) before submitting your proposal, so that we can be sure that you have what it takes to be a good Nightwatch.js contributor.
* Other form of contributions like helping out on Discord, GitHub issues, and reviewing pull requests are also most welcomed. We'd prefer contributors who can not only contribute to the codebase of Nightwatch.js but can also contribute to the community around it.
* Make sure to reach out and interact with the mentors to discuss your solution and approach towards a project idea before starting to fill in the proposal.
* Share the first draft of your proposal as early as possible.
* Share the proposal link as text, markdown, Google docs or anything else as long as it is easy to share, and will not require anyone to download something.
* Final proposals should be submitted on the Google Summer of Code website before the deadline and after all the reviews have been done.

## Starting out with Nightwatch.js

* First and foremost, try to fork, clone and setup the [Nightwatch](https://github.com/nightwatchjs/nightwatch) project (or any other project you wish to work on) locally.
* For most projects, you just need to run `npm i` to set them up locally.
* If working on the main Nightwatch project, try to run and play around with the example tests present in the project itself. You can find all the APIs available with Nightwatch in the [Nightwatch API Docs](https://nightwatchjs.org/api/).
* For e.g., to run the ecosia test, execute: `node ./bin/nightwatch examples/tests/ecosia.js --env chrome`.  

  __Note:__ When running Nightwatch example test for the first time, if you encounter _"Cannot read source"_ error, go to `nightwatch.conf.js` file and set 'page_objects_path' and 'custom_commands_path' configs to `[]`.
* If possible, take a quick glance through the Nightwatch [guide](https://nightwatchjs.org/guide/overview/what-is-nightwatch.html) and [API docs](https://nightwatchjs.org/api/) to get familiar with how the documentation is structured, which will help you later to find your answers more quickly.
* Contributions to improve docs and example tests are most welcomed :)

## Picking up and working on issues

* Please feel free to pick up any [good-first issues](https://github.com/issues?q=is%3Aissue+org%3Anightwatchjs+archived%3Afalse+label%3A%22good+first+issue%22+is%3Aopen) from the various Nightwatch.js repositories.
* Or, if you feel confident enough, you are welcome to help out with other non-labelled issues as well, but we'd suggest you to start with an easy issue.
* Always open __Draft__ PR and make sure to test your changes thoroughly in your local environment before marking your PR as ready for review. If you face any issues or don't understand something, feel free to reach out on Discord and ask for help.
* In order to handle the inflow of too many potential contributors and ensure timely resolution of the issues, we will only be assigning issues to contributors once they've looked into the issue and suggested a potential solution on the GitHub issue itself.
* While this might feel like it would lead to a lot of contributors wasting their time on an issue while only one of them will be able to create a final PR, please remember that we'll also be considering the quality of reviews a contributor leaves on other contributors' PRs while reviewing the final proposal, and investigating the issue yourself will help you post good PR reviews. __But please refrain from spamming the PRs with reviews, only good and quality reviews will be considered.__
* Moreover, in this process, you'll also get to explore and get familiar with the codebase of Nightwatch.js, which would help you with further issues.
* But still if you feel like you are leaving good reviews on other contributors' PRs but not getting to solve any issues on your own due to the speed at which others come up with the solution, please reach out us on Discord and we'll help find a suitable issue for you.

## Writing your proposal

* Your proposal should contain a clear understanding on how you're going to approach the project idea, along with a well-defined weekly schedule with clear milestones and deliverables around it.
* If you plan to propose your own project idea, please include a project outline, goals (as done in [Ideas List](GSoC-2024-Ideas.md)) and a well-defined weekly schedule with clear milestones and deliverables around it.

# Proposal Template

## Title of your project

### About Me

> Add your name, personal details and contact information (Discord id, E-Mail). Optionally, add why you would you consider yourself as the best person for this project.

### Past Experience

> Add your past coding experiences. Refer to any internship, freelance, professional or open-source work that you have did in the past (including personal projects).

### Past contributions

> Add your prior contributions to Nightwatch.js, including pull requests, bug reports, and helping others in the development community (can include any help on Discord, GitHub issues, or reviewing pull requests) with links to all materials, put together in a neat table and divided by appropriate projects.

## Project Proposal

### Abstract

> Add a short description of your project. Do not copy-paste from the official project description and add your perspective about the project as well. Do not exceed 10 lines of text. Define the problem/issue, express the current state and finally propose a solution.

### Motivation

> What is your motivation behind taking up this particular project and what excites you the most about it? What do you plan to achieve, personally or professionally, at the end of this project and how would you measure your success?

### Project plan

> Propose a clear list of deliverables along with all the technical intricacies and details. Optionally share your implementation plans as well, with architecture diagrams, code snippets and external references.
>
> Project plan should ideally be the most extensive portion of your proposal so make sure you define the solution for the problem you proposed above. It should clearly depict your understanding towards the project and how you plan to approach it.

### Schedule of Deliverables

> Document all your milestones, neatly divided into the various phases: before community bonding, during community bonding, Phase-1, Phase-2 and more. Each phase should be further divided into week-wise manner and sub-tasks should be added for all your deliverables to help mentors better understand the time estimate and if they are in accordance with the GSoC timeline.

### Additional Information

>Please include the answers to the following questions in your project application:
>
>* Why you’re excited about working on Nightwatch.js?
>* How does your availability look like during the GSoC period? Is there anything that you’ll be studying or working on whilst working alongside us?
>* How do you plan to stay connected with Nightwatch.js post the GSoC period?
