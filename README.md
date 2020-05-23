# azure-devops-flask
A simple template for deploying Flask apps with CI/CD to Azure DevOps


## Getting Started

This is still a WIP, so these instructions will be quick:

- Make new Resource group and create 3 new Azure App Services for your stages (flask-app-service-dev, flask-app-service-stg, flask-app-service-prod)
- Connect repo to DevOps by creating a new build pipeline and linking it to the repo. Set up CI from master branch.
- Builds should run based on the azure pipelines file within this repo whenever changes are made to master
- Set up Release Pipeline with three identical stages (dev, stg, prod). You'll have to select from the various dropdowns to connect the correct resources you made in step 1
- Optionally, set up CD in the dev stage of your release pipe. This will release any new changes to master branch to your dev webapp.
- Optionally, configure manual releases for stg or prod. This lets you have control over the promotion process.
