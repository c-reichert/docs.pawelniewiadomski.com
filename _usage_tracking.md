## Usage tracking

To support development of this plugin and understand better users limited usage tracking will be introduced in version 4.0.0. This plugin will report to Google Analytics only if [JIRA analytics is enabled](https://confluence.atlassian.com/jira062/data-collection-policy-588581615.html#Datacollectionpolicy-Enabling/disablingdatacollectioninJIRA).

The plugin will report following information:

- number and type of providers installed in the system (once a day)
- configuration changes - adding/removing/editing the provider
- occurence of an error during authentication
- initial installment of the plugin

You can always refer to [source code](https://github.com/pawelniewie/social-authentication-for-atlassian) to check how this information is gathered.

