# Dependabot-alerts-example
This repo is an example of how to aggregate the dependabot alerts data into the repositories

## How to use
In order to use this workflow, you will need to add the blueprints to your catalog. If you already have a repository blueprint, you will need to change a few things in the workflow, which will be listed further below.

After adding the blueprints, add the updateDependabot.yaml to the .github/workflows folder in your repository.

Next, you will need to add the action to the repository's blueprint. In the builder, expand the repository's blueprint and edit in JSON format. switch to the actions tab, and add the repositoryAction content inside the action's array.

Then, switch to the Scorecards tab, and add to the array the content of repositoryScorecard.

If you already have a repository blueprint, you will need to add a few properties. You can copy the properties from the repository.json file, from low_count to critical_count, or you can create them yourself manually.
If you decide to add them manually, make sure the properties identifier's are low_count to critical_count, accordingly.

After running the workflow, your repositories will ingest the data of the related Dependabot alerts, and the Scorecards will be updated.
