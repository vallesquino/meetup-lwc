# Lightning Web Components Example

1. Set up your environment. Follow the steps in the [Quick Start: Lightning Web Components](https://trailhead.salesforce.com/content/learn/projects/quick-start-lightning-web-components/) Trailhead project. The steps include:

  - Sign up for a Spring '19 pre-release org and enable Dev Hub
  - Install the pre-release version of the Salesforce CLI
  - Install Visual Studio Code
  - Install the Visual Studio Code Salesforce extensions, including the Lightning Web Components extension

2. If you haven't already done so, authenticate with your Spring '19 hub org and provide it with an alias (spring19hub):

  ```
  sfdx force:auth:web:login -d -a spring19hub
  ```

3. Clone the lwc-recipes repository:

  ```
  git clone https://github.com/trailheadapps/lwc-recipes
   cd lwc-recipes
  ```

4. Create a scratch org:

  ```
  sfdx force:org:create -s -f config/project-scratch-def.json
  ```

5. Push the app to your scratch org:

  ```
  sfdx force:source:push
  ```
6. Assign the **meetup_lwc** permission set to the default user:

  ```
  sfdx force:user:permset:assign -n meetup_lwc
  ```

7. Load sample data:

  ```
  sfdx force:data:tree:import --plan ./data/data-plan.json
  ```

8. Open the scratch org:

  ```
  sfdx force:org:open -p /lightning/n/Meetup_LWC
  ```
