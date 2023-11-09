# Dependabot-alerts-example
This repository is an example for calculating the amount of Dependabot alerts a repository has, and creating a Scorecard.

In this example, we use a Github workflow that sends requests to the search API of Port.

This guide is meant to be used after setting up the Github App. If you did not do that, head over to https://docs.getport.io/build-your-software-catalog/sync-data-to-catalog/git/github/installation

## How to use
### Resources
In this repository you can find a "Resource" folder, which will include all of the blueprints you will use in this guide.

To start, you will need to add the blueprints to your catalog. If you already have a repository blueprint, you will need to change a few things in the workflow, which will be listed further below.

After adding the blueprints, add the updateDependabot.yaml to the .github/workflows folder in your repository.

Next, you will need to add the action to the repository's blueprint. In the builder, expand the repository's blueprint and edit in JSON format. switch to the actions tab, and add the repositoryAction content inside the action's array.

Then, switch to the Scorecards tab, and add to the array the content of repositoryScorecard.

If you already have a repository blueprint, you will need to add a few properties. You can copy the properties from the repository.json file, from low_count to critical_count, or you can create them yourself manually.

If you decide to add them manually, make sure the properties identifier's are low_count to critical_count, accordingly.

Lastly, add the content of port-app-config.yaml to the Github mapping config. This will map the Dependabot Alerts from Github into Port.

### Running the workflow
After having everything set up, head to the Self Service page, and run the workflow. A Github job link will be added to it, where you can watch the logs of the workflow.

When the job is complete, the repositories Catalog page will be updated with the alerts count and Scorecards.

