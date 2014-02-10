## Continuous Delivery Strategy ##

### Configuration Management ###
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

### Continuous Integration ###


