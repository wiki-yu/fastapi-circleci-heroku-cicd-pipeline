# FastAPI APP + CircleCI + Heroku Deployment Example


## Setup enviroment:

_For Windows:_

```bash
py -m venv env # Only run this if env folder does not exist
.\env\Scripts\activate
pip install -r requirements.txt
```

_For MacOS/Linux:_

```bash
python3 -m venv env # Only run this if env folder does not exist
source env/bin/activate

pip install -r requirements.txt
``````

## Setup Heroku
1. Create an account on Heroku
2. Create new app on Heroku
3. Check "Heroku git URL" for you app, later it will be used for 
4. Check API key from "Account Setting", later it will be used for recognizing your Heroku account in CircleCI.
Notes: Check doc/AI_Deployment_Heroku.doxc for more details.

## Setup CicleCI
1. Connect CircleCI with Github
  * Create a CircleCI account linking your Github

2. Connect CircleCI with Heroku
  * Click “Project Setting” for the corresponding Github project. 
  * Set up “Environment Variable” to connect CircleCI and Heroku, so that CircleCI knows your Heroku info. (The ENV name should match the one from the config.yml file. The value is obtained from the API key on Heroku.)
Notes: More details and some screenshot, check doc/CICD_CircleCI.docx

## Setup .circleci/config.yml file
Here you define the CICI pipeline and other details

## Check Deployment
Open APP on Heroku to check if the application is deployed automatically 


