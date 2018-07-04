# Welcome to the docker wiki!

[![Codefresh build status]( https://g.codefresh.io/api/badges/build?repoOwner=shaeenk&repoName=docker&branch=master&pipelineName=docker&accountName=shaeenk&type=cf-1)]( https://g.codefresh.io/repositories/shaeenk/docker/builds?filter=trigger:build;branch:master;service:5b3d07769fe801465af799c2~docker)
![Docker Automated build](https://img.shields.io/docker/automated/jrottenberg/ffmpeg.svg)

_Any changes made and pushed up to this repository will automatically trigger a build on my docker hub and within a couple of minutes later the build would of completed_.

## Requirements

* Jenkins
* Blue Ocean plugin installed

## Enviroment Setup

### Jenkins Docker Permissions
Open up the terminal and add in the following command 
`sudo usermod -aG docker jenkins`

The above command gives jenkins the correct permissions to use Docker commands

Restart the Jenkins service once you've ran the command

## Creating Pipeline

### Pipeline Repository Setup Steps
1. Create a Personal access token that gives blue ocean access to your repositories (_token is only used once unless it is deleted/removed or your Jenkins was uninstalled_).
2. Select the Repo your want to test (_Make sure that the repo you are testing doesn't have an existing Jenkinsfile in it_).
3. Click the Agent drop down and select docker.
4. In the **_Image *_** field add in `shaeenk/docker`.
5. Add in the step you need that will be running you test script
