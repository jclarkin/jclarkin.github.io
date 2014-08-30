---
layout: post
title: Research Session - Javascript Unit Testing
date: 2014-03-12
categories:
- Testing
tags: []
status: publish
type: post
published: true
meta:
  _publicize_pending: '1'
author: 
---
**Report Summary**:

*   Much like the rest of the Javascript ecosystem, there are a lot of options for any given problem and not a lot of community consensus
*   There are two aspects of JS testing needing to be addressed: tools to test (libraries) and tools to report results (test runners)
*   When selecting libraries, there are two style choices: [TDD](http://en.wikipedia.org/wiki/Test-driven_development) (Test Driven Development) vs. [BDD](http://en.wikipedia.org/wiki/Behavior-driven_development) (Behaviour Driven Development)

    Historically, our company has been more comfortable with TDD
*   [Chai.js](http://chaijs.com/) is a TDD library that looks like a good place to begin learning and experimenting with test authoring
*   Still not sure of pros/cons between test runners
*   Further analysis plans

    *   Follow up with this question to the [OttawaJS](http://ottawajs.org/) community on March 20th
    *   Attend [Webinar on theintern.io](http://www.sitepen.com/site/intern.html) on March 20th
    *   Experiment with TDD library [Chai.js](http://chaijs.com/) and its test runner
    *   Experiment with test runner [theinter.io](http://theintern.io/)

Session notes below the fold...

------

**Mission**: To determine and select tools for Javascript test scripting

**Charter**:

*   Google search for tool options
*   Explore theintern.io (mentioned by an awesome colleague)
*   Compare QUnit vs. Jasmine (previous knowledge)

**Recording of Session**:

*   Found [this StackOverflow post](http://stackoverflow.com/questions/300855/javascript-unit-test-tools-for-tdd) with a large list of tools. Looks a bit out of date, but is a good start.

*   [Jasmine](http://jasmine.github.io/) supports [BDD](http://en.wikipedia.org/wiki/Behavior-driven_development). Comes with equivalent ideas to [Hamcrest Matchers](http://hamcrest.org/JavaHamcrest/). Our dev team has not yet successfully assimilated BDD, so this is not a strong incentive for adoption.

*   [QUnit](http://qunitjs.com/) site has some good material on refactoring code to become scriptable. Pretty execution display as an HTML file. Not seeing the big picture on how this would work in a CI environment.

*   If we are just looking for a library to make assertions easier (like JUnit) then bare-bones might be the best.

*   [Chai.js](http://chaijs.com/) seems like a lightweight assertion library. Worth consideration for initial practice authoring testable code.

*   [BrowserSwarm](http://www.browserswarm.com/) is very cool. But it is a commercial offering of [TestSwarm](http://testswarm.signalr.net/). TestSwarm is also cool. A tool where any device can register to the swarm to execute JS test files. The project does not look highly active.... Is this due to it being fairly stable or that people have found a different path?

*   This brings a key question to light: test execution and reporting methods. This is really going to be the key to valuable tests...

*   On to touch base with [Wiki list of JS Test frameworks](https://en.wikipedia.org/wiki/List_of_unit_testing_frameworks#JavaScript)

    To further explore: Unit.js, Mocha, Sinon.js

*   [Unit.js](https://en.wikipedia.org/wiki/Unit.js) looks similar to Chai.js and Jasmine.

*   [Mocha.js](http://visionmedia.github.io/mocha/) is not a library, but a framework. It runs on Node, and is popular amongst the OttawaJS presenters last year. Uses 4 libraries to offer Asserts and BDD notation in test cases (should.js, expect.js, chai.js, &amp; better-assert). Comes with classic JUnit style before/after/beforeEach/afterEach. Pretty reporting to the console, or a variety of formats (TAP, JSON, CLI, HTML, XUnit, ...).

*   Sinon.js is a library in the vein of Mockito. Looks handy... but too advanced for our current needs. Keep in mind if mocking topic comes up.

*   Onto look into [theintern.io](http://theintern.io), from Dave. He sent a webinar for March 20th (I've signed up). Now on to exploring the site/examples.

    *   Looks to provide Test Execution with test authoring. Uses chai.js for asserts and expect.js for behaviour. Looks similar to authoring JUnit tests, with BDD and TDD support. Examples of how to have it execute Selenium over remote. Examples of using [SauceLabs](https://saucelabs.com/) for multi-platform testing (Saucelabs not available for intranet activities). Good [example of code here](https://github.com/theintern/intern-tutorial).
    *   Test running can be Node, your browser, SauceLabs, Selenium Grid
    *   [theintern.io](http://theintern.io) seems the most promising at this point and worth deeper investigation (hands on experimentation).

*   Listened to the recent [Hanselminutes podcast](http://hanselminutes.com/412/getting-started-with-javascript-unit-testing-with-jasmine-and-rushaine-mcbean) on Javascript UT. Focused on explaining Jasmine, and BDD. Was interesting and pointed out that there are add-ons for Jasmine to tackle specific JS things (like jQuery and ajax).