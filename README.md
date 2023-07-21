# Trello Enterprise - Non-Enterprise Workspace Cleanup

This is an open source script to help you pull in all non-enterprise workspaces into your workspace. This ensures that all content created by users managed by your Enterprise (but are free), is covered by your security settings. This script also deactivates users who have not been active in X days, when pulling in each workspace. For more details on how exactly to use this script, see details below. 

---
### User Paramaters 
There are 3 variables that the user must input for the script to work:
- **API Token** - This is the API token used to authenticate that the script has permission to run the needed operations against the chosen Enterprise. The API token must be tied to a user of the Enterprise with Enterprise Admin Permissions. Make sure that your API token includes write permissions. See the [Trello API documentation](https://developer.atlassian.com/cloud/trello/guides/rest-api/api-introduction/)
 for more details. 
- **API Key** - This is the API Key used to authenticate that the script has permission to run the needed operations against the chosen Enterprise. The API token must be tied to a user of the Enterprise with Enterprise Admin Permissions. See the [Trello API documentation](https://developer.atlassian.com/cloud/trello/guides/rest-api/api-introduction/)
- **Enterprise ID** - This is the ID of the Enterprise that the user would like to run the script against. See the [Trello API documentation](https://developer.atlassian.com/cloud/trello/guides/rest-api/api-introduction/)
 
In addition there below are a few customizations you can make if you would like. 
- **daysSinceLastActive** - This variable defines how you want to define activity and will impact which users will get deactivated from the Enterprise. If a user has not been active in the last X days (aka X days or more) then they will be deactivated. This will remove them from all Enterprise Workspaces and take away their Enterprise seat. 


---
### Outputs
When this script is run, it will output two different report files:
- **Post-run_workspace report** - This is the CSV file that captures all the non-Enterprise workspaces that were added to the Enterprise.
- **Post-run_member_report** - This is the CSV file that is generated after to keep track of the users who were given an Enterprise seat as a result of them beign part of a non-Enterprise workspace that got added to the enterprise, and which of those users were deactivated after being added to the enteprise because they were not active. 

## Have Questions?
Post on the Atlassian Community [here](https://community.atlassian.com/t5/Trello/ct-p/trello) and tag @Alexandros Mathopoulos.
