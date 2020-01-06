# databricks_automation
This is an example of a full databricks CI/CD pipeline leveraging Azure DevOps Pipelines

The pipeline leverages Keyvault for all needed parameters and secrets.  You will need to setup a Variable Group linked to Keyvault for this pipeline to pull in the secrets.
The pipeline creates a DataBricks PAT token, creates a Data Bricks cluster, runs the databricks notebook, destroys the cluster.
This can be linked to a PR request to run to verify the notebook before approval.   After approval a trigger can be setup to deploy the notbook to a staging or production DataBricks workspace.
