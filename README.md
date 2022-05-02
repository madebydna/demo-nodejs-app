Sample NodeJs Application
------------------------

## Overview

CI/CD to test, build, push and deploy the NodeJS Dokerized app to AWS ECS using Jenkins Declarative Pipeline.

## Tech Stack

1. Github

This contains our sample nodes application code.

2. Jenkins

Jenkins declarative pipeline that is triggered on every commit.

3. ECR

Docker images will be stored in AWS ECR.

4. ECS

Aplication will be deployed in AWS ECS.


## Pipeline Stages

1. Test repo by running `npm test` after installing dependencies

2. Build an image with `docker.build` (using Docker Pipeline plugin syntax)

3. Push the image to ECR with `docker.withRegistry` (using Docker Pipeline plugin syntax)

4. Deploy the image with `withAWS` (using [Pipeline: AWS Steps](https://plugins.jenkins.io/pipeline-aws/#plugin-content-withaws) plugin)


## Notes
