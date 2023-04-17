# dr-streamlit

First draft of DataRobot Streamlit. 

## Getting started:
### What's included in here:
We have two basic streamlit apps: `prediction_form_example` and `insights_app_example`. 
The prediction form example is a default app which lets a user submit a single prediction using the real time DataRobot generated prediction explanations and color-coded n-grams. 
or batch prediction API and provides. Some projects (like SHAP) project need to use the batch prediction API. 
The insights app lets a user view models in the leaderboard and view their word cloud and feature  impact charts. The word cloud has a special breakdown
for individual text features as well.
### What's supported
At the moment we want to support Multiclass, Regression, and Binary projects. Some projects (like SAFER) should work, but we don't want to focus 
on Multiclass, Regression, and Binary at the moment. 
### Running on a local computer:
The required dependencies should be defined in requirements.txt, and are instalable via your favorite package manager( eg:  `pip install -r requirements.txt` )
Next you need to supply the token, project id or deployment id. These can either be hard set in the code or be environment variables like `token`, `projectid`, or `deploymentid`.
The project/deployment ID are part of the URL in DataRobot and you have developer tokens under your Developer tools (https://app.datarobot.com/account/developer-tools)

### Running on hosted streamlit
https://share.streamlit.io/ has a dashboard for hosting streamlit
Point it at the streamlit file you want to run, and under `Advanced Settings` just enter your project or deployment id and your token like:
```
projectid = "<your id>"
token = "<your token>"
```
and streamlit's deployment should take care of the rest

