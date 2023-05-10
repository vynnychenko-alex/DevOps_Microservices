[![CircleCI](https://dl.circleci.com/status-badge/img/gh/vynnychenko-alex/DevOps_Microservices/tree/master.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/vynnychenko-alex/DevOps_Microservices/tree/master)

## Repository Overview

This repository provides code to encapsulate a Python-based machine learning application into a container. The application utilizes a pre-trained sklearn model, specifically designed to predict housing prices in Boston based on various features like average rooms, highway access, and teacher-to-pupil ratios. Additional details about the dataset used can be found on the data source site, which originally obtained the data from Kaggle.

`app.py`— serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

---

## Setup the Environment

* Create a virtualenv with Python 3.7 and activate it. Refer to this link for help on specifying the Python version in the virtualenv. 
```bash
python3 -m pip install --user virtualenv
# You should have Python 3.7 available in your host. 
# Check the Python path using `which python3`
# Use a command similar to this one:
python3 -m virtualenv --python=<path-to-Python3.7> .devops
source .devops/bin/activate
```
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl
