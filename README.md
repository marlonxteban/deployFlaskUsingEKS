# Deploying a Flask API

This is my final repo for the fourth course in the [Udacity Full Stack Nanodegree](https://www.udacity.com/course/full-stack-web-developer-nanodegree--nd004): Server Deployment, Containerization, and Testing.

The Flask app used for this project consists of a simple API with three endpoints:

- `GET '/'`: This is a simple health check, which returns the response 'Healthy'. 
- `POST '/auth'`: This takes a email and password as json arguments and returns a JWT based on a custom secret.
- `GET '/contents'`: This requires a valid JWT, and returns the un-encrpyted contents of that token. 

The app relies on a secret set as the environment variable `JWT_SECRET` to produce a JWT.

## Initial setup
1. Fork this project to your Github account.

## Dependencies

- Docker Engine
- AWS Account
     
## Project Content

This repo contains:
- requirements.txt: requirements for running the tests and the main app.
- dockerfile: you can test create a container in your local environment and test the app.
- test_mai.py: tests for the app.
- main.py: main app.
- ci-cd-codepipeline.cfn.yml: template for create a stack in aws CloudFormation.
- buildspec.yml: file that specifies aws CodeBuild pipeline.
- simple-jwt-api.yml: pods specs applied in builspec.yml.
