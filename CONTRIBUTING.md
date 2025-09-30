# How to Contribute

We welcome contributions to the **ServiceNow Developer Program's ActionPack Repository**! Follow these steps to get involved:

## Contributions for Hacktoberfest 2025
In Hacktoberfest 2025, we are looking for Flow Action submissions only. When committed to source control, these are seen as `sys_hub_action_type_definition_{sys_id}.xml` files, where sys_id is the unique ID of the action definition.

Any contributions that add or change other files will be flagged as `non-compliant` and automatically closed. This allows us to streamline the process from the perspective of our maintainers. If you wish to introduce separate object types, please reach out to Astrid Sapphire (@SapphicFire), who can validate your request and accept PRs of this nature.

## Steps to Contribute

1. **Fork the Repository**: Click the "Fork" button on the top right of this page to create your own copy of the repository.

2. **Go to your ServiceNow instance**: Log in to your ServiceNow instance

3. **Optional - Create a credential for GitHub**: If you have not used Source Control in this instance before, create a credential as described by Earl [here](https://www.servicenow.com/community/developer-advocate-blog/source-control-in-servicenow-studio-complete-walkthrough/ba-p/3356303#create-a-credential-in-servicenow).

4. **Recommended - Install the ServiceNow IntegrationHub Enterprise Pack Installer plugin**: In order to access all step types available to actions, ensure the `ServiceNow IntegrationHub Enterprise Pack Installer` plugin is installed. To do so, use the below links based on whether you are working from a PDI or Customer/Vendor instance:
   - **Customer/Vendor**: Install the plugin from Now Support using the Automation Store: [ServiceNow IntegrationHub Enterprise Pack Installer](https://support.servicenow.com/now/en/pages/automation-store?id=ns_automation_store&plugin_sys_id=752e0d351b2d90101c8633f2cd4bcbc4) 
   - **PDI**: Install the plugin from the Developer site using the Manage Instance page: [Manage Instance](https://developer.servicenow.com/dev.do#!/manage-instance)

5. **Import ActionPack into your instance**: Using a Source Control-enabled Studio, import your fork of this repository from source control using the `main` branch. Steps and compatible studios are listed below:
  - **Studios**:
    - On Zurich and above: `ServiceNow Studio`
    - On Yokohama and earlier: `App Engine Studio` or `Legacy Studio`
  - **Steps**:
    - [SNS Import Instructions](http://servicenow.com/docs/bundle/zurich-application-development/page/build/servicenow-studio/task/sns-sc-import-app-source-control.html)
    - [AES Import Instructions](http://servicenow.com/docs/bundle/yokohama-application-development/page/build/app-engine-studio/task/source-control-import.html)
    - [Legacy Studio Import Instructions](https://www.servicenow.com/docs/bundle/yokohama-application-development/page/build/applications/task/t_ImportAppFromSourceControl.html)

6. **Create a New Branch**: Using a Source Control-enabled studio, create a new branch and switch to it. Name your branch according to the functionality you are adding (e.g., `feature/new-snippet` or `bugfix/fix-issue`). Steps are listed below:
   - [SNS Create Branch Instructions](https://www.servicenow.com/docs/bundle/zurich-application-development/page/build/servicenow-studio/concept/sns-sc-create-versions-branches-git.html#title_sns-sc-create-repo-branch)
   - [AES Create Branch Instructions](https://www.servicenow.com/docs/bundle/yokohama-application-development/page/build/app-engine-studio/concept/create-versions-branches-git.html#title_source-control-create-branch)
   - [Legacy Studio Create Branch Instructions](https://www.servicenow.com/docs/bundle/yokohama-application-development/page/build/applications/task/t_CreateBranch.html)

7. **Add or Edit a Flow Action**: Using your preferred studio experience, create a new action or update an existing action.

8. **Commit your contribution to Source Control**: Using a Source Control-enabled Studio, commit your changes to source control. Steps are listed below:
   - [SNS Commit Changes Instructions](https://www.servicenow.com/docs/bundle/zurich-application-development/page/build/servicenow-studio/task/sns-sc-commit-changes-to-repository.html)
   - [AES Commit Changes Instructions](https://www.servicenow.com/docs/bundle/yokohama-application-development/page/build/app-engine-studio/task/source-control-commit-changes.html)
   - [Legacy Studio Commit Changes Instructions](https://www.servicenow.com/docs/bundle/yokohama-application-development/page/build/applications/task/t_CommitChanges.html)

9. **Submit a Pull Request**: In GitHub, submit a new pull request against the `main` branch of ActionPack, from your fork and branch. Steps are listed below:
   - Go to the original repository and click on the "Pull Requests" tab.
   - Click "New Pull Request" and select your branch.
   - Ensure your pull request has a descriptive title and comment that outlines what changes you made.
   - Only include files relevant to the changes described in the pull request title and description.
   - Avoid submitting XML exports of ServiceNow records.

That's it! A Developer Advocate or a designated approver from the ServiceNow Dev Program will review your pull request. If approved, it will be merged into the main repository for everyone's benefit!

### Note on Multiple Submissions
If you plan to submit another pull request while your original is still pending, make sure to create a new branch in your forked repository first.

## Automations and File Type Restriction

In 2025, GitHub Action automations are being introduced across key repositories to facilitate smoother maintenance. As ActionPack is only open for introducing Flow Actions, an automation has been configured that checks for changed files. If the files that are changed are not permitted (anything except `sys_hub_action_type_definition_{sys_id}.xml` and `checksum.txt`), the PR automation will identify this, add a comment and label, then close the PR as non-compliant. 

Developers are welcome to re-open their PRs once invalid files have been removed.

## General Requirements

- **Descriptive Pull Request Titles**: Your pull request must have explicit and descriptive titles that accurately represent the changes made.
- **Scope Adherence**: Changes that fall outside the described scope will result in the entire pull request being rejected.
- **Quality Over Quantity**: Low-effort or spam pull requests will be marked accordingly.
- **Expanded Flow Actions**: Flow actions introduced that replicate existing Scopes or Global actions are acceptable only if they are expanded in a meaningful way (e.g., with additional functionality or variations). Remember: *“QUANTITY IS FUN, QUALITY IS KEY.”*
- **Relevance**: Flow actions should be relevant to ServiceNow Developers.

Thank you for contributing! Your efforts help create a richer resource for the ServiceNow development community.