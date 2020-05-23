# azure-devops-flask
A simple template for deploying Flask apps with CI/CD to Azure DevOps


## Getting Started

This is still a WIP, so these instructions will be quick:

### Make new Resource group and create 3 new Azure App Services for your stages (flask-app-service-dev, flask-app-service-stg, flask-app-service-prod)

![Resource Overview](https://github.com/nateraw/azure-devops-flask/blob/master/images/resource_overview.png)

- Connect repo to DevOps by creating a new build pipeline and linking it to the repo. Set up CI from master branch.
- Builds should run based on the azure pipelines file within this repo whenever changes are made to master
- Set up Release Pipeline with three identical stages (dev, stg, prod). You'll have to select from the various dropdowns to connect the correct resources you made in step 1
- Optionally, set up CD in the dev stage of your release pipe. This will release any new changes to master branch to your dev webapp.
- Optionally, configure manual releases for stg or prod. This lets you have control over the promotion process.

### Additional Images

### This is the structure of the release pipeline

![Resource Overview](https://github.com/nateraw/azure-devops-flask/blob/master/images/release_pipe_overview.png)

### You'll want to have settings similar to the next two images...

This shows the steps you'll need to add

![Resource Overview](https://github.com/nateraw/azure-devops-flask/blob/master/images/release_pipe_settings_1.png)

This one shows how I configured it (minus my subscription ID which my resource group falls under)

![Resource Overview](https://github.com/nateraw/azure-devops-flask/blob/master/images/release_pipe_settings_2.png)

You can play with deployments and keep an eye on which ones are deployed to which environments via your release pipeline overview page.

![Resource Overview](https://github.com/nateraw/azure-devops-flask/blob/master/images/release_pipe_status.png)
