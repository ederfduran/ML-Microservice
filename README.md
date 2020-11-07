[![CircleCI](https://circleci.com/gh/ederfduran/ML-Microservice.svg?style=svg)](https://app.circleci.com/pipelines/github/ederfduran/ML-Microservice)

## Project Overview

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

## Requirements

- python
- flask
- Docker
- minikube
- Hadolint

## What's in the repo?

This is a most relevant files that you most be aware of:

- `app.py`: Here is where all code logic resides. Flask is used to expose a trained model capabilities using an API.
- `Makefile`: This file describes some important tasks such as build, lint, test and run. It is used to automate the process of execute these tasks.
- `Dockerfile`: Describe the steps to Build the image and containerized the application.
- `run_docker.sh`: Shell file used to build image described in docker file and also to run it as a container
- `upload_docker.sh`: Shell file used to push the image into dockerhub and int that way use it later on in kubernetes cluster.
- `run_kubernetes.sh`: Run the app in kubernetes cluster using kubectl and image previously saved in dockerhub.
- `make_prediction.sh`: make an POST request in our API in order to make a prediction.

## Setup the Environment

- Create a virtualenv and activate it
- Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone: `python app.py`
2. Run in Docker: `./run_docker.sh`
3. Run in Kubernetes: `./run_kubernetes.sh`

### Kubernetes Steps

- Setup and Configure Docker locally
- Setup and Configure Kubernetes locally
- Create Flask app in Container
- Run via kubectl
