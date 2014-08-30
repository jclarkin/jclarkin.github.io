---
layout: post
title: Research Session - JS UT Experimentation
date: 2014-03-21 15:18:08.000000000 -04:00
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
Recommend starting with [Chai.js](http://chaijs.com/) + [Mocha](http://visionmedia.github.io/mocha/)ß, and [Sinon.js](http://sinonjs.org/) for mocking when necessary.

A lot of the test libraries available are similar, so it is hard to go wrong. Chai.js appears to be commonly used and also integrated into larger frameworks. Since Chai is just a test authoring library, there is still need for a tool to execute the tests. For current needs, Mocha has good support and a lot of reporting output options. At this point, the added benefits provided by theintern.io do not add immediate value for me, but transitioning to it from Mocha should not be difficult.

Further analysis plans
*   Look into Test Runner outputs and how they might integrate into JUnit reports

Simplistic examples created during experimentation can be found on [Github here](https://github.com/jclarkin/javascript-test-frameworks).


Session notes below the fold...

------

**Mission**: Attempt to create JSUT (Javascript Unit Test) using simple libraries

**Charter**:

*   Create some executable tests using [Chai.js](http://chaijs.com/)
*   Follow traditional JUnit TDD patterns rather than BDD
*   (added) Explore BDD experiments as well

**Session**:

*   Start: March 19, 2014

*   Experiment: Attempted to figure out [Chai.js](http://chaijs.com/)
*   Fail: could not solve how to run the tests

*   Experiment: Moving on to [QUnit](https://qunitjs.com/) to warm my experience
*   Success: got a simple sample of QUnit tests and runner executing
*   Discovery: Chai.js does not have a test runner. We need to pick one to execute the chai tests

*   Experiment: Chai.js with Mocha as the test runner
*   Fail: Having trouble setting it up.
*   Learn: Found these [cool chai.js plugins](https://github.com/Bartvds/chai-tdd-plugins) that could be useful: helpers for statistics, jquery, http processing, and more
*   Learn: Found [this article](https://gist.github.com/maicki/7781943) to help me out
*   Success: After much initial confusion, I have successfully authored some simple tests that I can run via HTML in a browser
*   Learn: Visit from [@snocorp](https://twitter.com/snocorp) has convinced me that it is silly to ignore BDD due to historic corporate aversion to change
    Increasing the charter to include BDD experimentation

*   Experiment: Create a BDD version of the chai-mocha tests
*   Fail: Trouble getting the 'throw' scenario to work...
    Trying a success and fail case to ensure my understanding...
*   Success: Added test cases for both throw and not throw to ensure understanding

*   Experiment: Setup a [Jasmine](http://jasmine.github.io/) test suite (BDD library and runner combined)
*   Success:
    *   very easy to use
    *   nearly identical to the chai-mocha-bdd experiment
*   Learn: Based on my initial research report, there exists [Unit.js](http://unitjs.com/)
    *   I misunderstood it with initial research
    *   It is a library that contains the following micro-libraries
        *   Mocking via [Sinon.js](http://sinonjs.org/)
        *   BDD via [Must.js](https://github.com/moll/js-must) + [Should.js](https://github.com/visionmedia/should.js/) + [Expect.js](https://github.com/LearnBoost/expect.js/)
    *   TDD via [Node assert](http://nodejs.org/api/assert.html)
    *   It does not have a Test Runner, but it recommends Mocha as a decent starting point
*   Paused - End of workday

*   Start: March 20, 2014

*   Learn: Audit the "theintern.io" webinar
    *   Good presentation
    *   An alternate Test Runner to mocha
    *   Supports JS tests and Selenium (may require setting up a Selenium Grid to communicate to)
    *   Easy integration to Saucelabs (which can work in a secured environment via a secured tunnel)
    *   Covered AJAX mocking using AMD and replacing the default map of loaders at Setup, and reverting at teardown
    *   Framework built with Dojo
    *   Chai for assertions
    *   Istanbul for Code coverage
    *   Need to research and better understand Test Reports/Outputs
*   Learn: Attended OttawaJS Meetup
    *   Confirmed that my research is on the right tools/libraries/frameworks
    *   Was recommended to look into [Karma](http://karma-runner.github.io/) test runner (previously called Testacular)
*   Paused - End of workday

*   Start: March 21, 2014
*   Learn: Karma test runner
    *   Looks as good for test running as the alternative so far
    *   Has nice automation abilities similar to [Grunt](http://gruntjs.com/)
    *   Requires [Node.js](http://nodejs.org/)
*   Explain: Create summary of research
*   Share: Place learning material into a [public repo](https://github.com/jclarkin/javascript-test-frameworks) for others to also learn from it