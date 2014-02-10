## Continuous Delivery Strategy ##
I. [**Foundations**](https://github.com/nateleavitt/mindump/blob/master/cdelivery/strategy.md#i-foundations)

1. [Configuration Management](https://github.com/nateleavitt/mindump/blob/master/cdelivery/strategy.md#1-configuration-management)
2. [Continuous Integration](https://github.com/nateleavitt/mindump/blob/master/cdelivery/strategy.md#2-continuous-integration-ci)
3. [Implementing a Test Strategy](https://github.com/nateleavitt/mindump/blob/master/cdelivery/strategy.md#3-implementing-a-testing-strategy)

II. [**The Deployment Pipeline**](https://github.com/nateleavitt/mindump/blob/master/cdelivery/strategy.md#ii-the-deployment-pipeline)

III. [**The Delivery Ecosystem**](https://github.com/nateleavitt/mindump/blob/master/cdelivery/strategy.md#iii-the-delivery-ecosystem)

## I. Foundations ##
### 1. Configuration Management ###
With a good configuration management strategy we should be able to answer 'yes', to following questions questions (pg 32)
* can I exactly reproduce any environments? (OS, network config, software stack, apps, etc..)
* can I easily make incremental changes to any of those items?
* can I easily see these changes and who made them?
* can I satisfy all compliance regulations?
* is it easy for every team member to get info they need, and to make the changes they need?

Strategy for storing baselines and controlling changes to:
* apps source code, build scripts, tests, documentation, requirements, database scripts, libs, config files
* dev, testing, and ops toolchains
* all environments used in dev, testing, and production
* entire application stack - both binaries and configuration
* config associated with every app in every environment it runs in, across the entire app lifecycle (building, deploy, test, operation)

### 2. Continuous Integration (CI) ###
The goal of continuous integration is that the application is in a working state all the time. CI is a practice NOT a tool!
* represents a paradigm shift - Your software is broken until somebody proves it works, usually during a testing or integration stage
* the application is built and comprehensive tests are run against it on every commit

Benefits of CI
* deliver software much faster
* fewer bugs - bugs are caught much earlier in delivery process
* cheaper to fix - significant cost and time savings

Three things needed before CI implementation
* version control
* an automated build - be able to build and run test scripts from the command line.. apart from IDE
* agreement of team - smaller commits, more often.. it is a practice not a tool

Essential Practices
* do not check in a broken build
* always run all commit tests locally before committing
* wait for commit tests to pass before moving on
* never go home on a broken build
* always be prepared to revert to previous revision
* time-box fixing before reverting (10 min?)
* do not comment out failing tests
* take responsibility for all breakages that result from your changes
* test driven development

### 3. Implementing a Testing Strategy ###
Testing is a function that involves multiple teams and should be done continuously. Building quality in means writing automated tests at multiple levels (unit, component, and acceptance) and running them as part of the deployment pipeline, which is triggered every time a change is made to the application. Manual testing is also essential part of building quality in: Showcases, usability testing, and exploratory testing.
* Automated tests are run by CI server - should also include tests for security and capacity

Benefits of a good testing strategy
* establishes confidence that the software is working the way it should
* fewer bugs
* reduced support cost
* improved reputation

Types of tests
* Business-facing tests that support the development process (functional and acceptance tests)
* Technology-facing tests that support the development process (unit, functional, and deploy tests)
* Business-facing tests that critique the project (manual QA testing and user testing)
* Technology-facing tests that critique the project (functional and non-functional tests - capacity, security, etc..)
* Test Doubles (stubs, mocks, etc..)

## II. The Deployment Pipeline ##
## III. The Delivery Ecosystem ##
