# Trello-Enterprise-Inactive-Non-Enterprise-Workspace-Cleanup

This is an open source script to help you bulk managed your Trello users using the Trello API. Using this script you can give Enterprise seats to Free Managed Members active in the last X days (example - 90 days). You can customize how you define active. For more details on how exactly to use this script, see this video below: 

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/XBQXbzUa5qE/0.jpg)](https://www.youtube.com/watch?v=XBQXbzUa5qE) 
---
### User Paramaters 
There are 3 variables that the user must input for the script to work:
- **API Token** - This is the API token used to authenticate that the script has permission to run the needed operations against the chosen Enterprise. The API token must be tied to a user of the Enterprise with Enterprise Admin Permissions. Make sure that your API token includes write permissions. See the [Trello API documentation](https://developer.atlassian.com/cloud/trello/guides/rest-api/api-introduction/)
 for more details. 
- **API Key** - This is the API Key used to authenticate that the script has permission to run the needed operations against the chosen Enterprise. The API token must be tied to a user of the Enterprise with Enterprise Admin Permissions. See the [Trello API documentation](https://developer.atlassian.com/cloud/trello/guides/rest-api/api-introduction/)
- **Enterprise ID** - This is the ID of the Enterprise that the user would like to run the script against. See the [Trello API documentation](https://developer.atlassian.com/cloud/trello/guides/rest-api/api-introduction/)
 
In addition there are 5 customizations that the user can customize if they would like: 
- **testRun** - This script has a testRun mode. When testRun is set to true, the script will simulate giving Enterprise Seats and give you a pre_run csv report but will not actually give any users Enterprise Seats. When testRun is set to false, it will actually give enterprise seats to those users meet your activity paramater (see below).
- **runOnlyOnce** - This script can be configured to run 1x or if they user would like, run every X number of days. Set this value to true to run only once and false to run every X number of days. 
- **IntervalDays** - If the runOnlyOnce is set to false, then how often would you like the script to run. Enter this in number of days. 
- **daysSinceLastActive** - This variable defines how you want to define activity. By default this is set to 90 days. 
- **batchCount** - This variable allows you to define how many users you want to give Enterprise seats at once. The default value is 100. We do not recommend going much higher than this because you may get rate limited.

---
### Outputs
When this script is run, it will output two different report files:
- **Pre-run member report** - This is the CSV file that is generated before any members are actually given Enterprise seats. Review this report if you have set your testRun value to true.
- **Post-run member report** - This is the CSV file that is generated after to keep track of every user who has been given an enterprise seat. Review his report to understand which users where given a seat after the script is done running. This report is is only generated if testRun is set to false.

## Have Questions?
Post on the Atlassian Community [here](https://community.atlassian.com/t5/Trello/ct-p/trello) and tag @Alexandros Mathopoulos.
