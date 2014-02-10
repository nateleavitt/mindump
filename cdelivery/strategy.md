## Continuous Delivery Strategy ##

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

Three things needed before being CI implementation
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
