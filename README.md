# FastAPI APP + CircleCI + Heroku Deployment Example

## Setup Heroku
1. Create an account on Heroku
2. Create new app on Heroku
3. Check "Heroku git URL" for you app, later it will be used for 
4. Check API key from "Account Setting", later it will be used for recognizing your Heroku account in CircleCI.
Notes: Check doc/AI_Deployment_Heroku.doxc for more details.

## Setup CicleCI
1. Connect CircleCI with Github
Create a CircleCI account linking your Github

2. Connect CircleCI with Heroku
(1) Click “Project Setting” for the corresponding Github project. 
(2) Set up “Environment Variable” to connect CircleCI and Heroku, so that CircleCI knows your Heroku info. (The ENV name should match the one from the config.yml file. The value is obtained from the API key on Heroku.)
Notes: More details and some screenshot, check doc/CICD_CircleCI.docx

## Setup .circleci/confi.yml file
Here you define the CICI pipeline and lots of other details









## Installation

### Setup Virtual Environment

```shell
virtualenv -p python3.7 env
source ./env/bin/activate
```

### Install Dependencies

```shell
pip install -r requirements.txt
```

## Run the application

```shell
uvicorn app.main:app --host 0.0.0.0 --port 8080 --reload
```

## Deploy

### Package Dependencies

```shell
cd env/lib/python3.7/site-packages
zip -r9 /path/to/root/function.zip
```

### Package Lambda

```shell
cd /path/to/root
zip -g function.zip lambda_function.py
```
