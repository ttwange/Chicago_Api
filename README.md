# Chicago_Api
API data pipeline to Google Cloud storage using Mage AI

Chicago Crimes api: https://data.cityofchicago.org/resource/xguy-4ndq.csv
In this project we will be creating an API pipeline to extract data from City of Chicago Data to Google Cloud storage (this will act as the data lake). The pipeline will be orchestrated using Mage AI. 
Prerequisites:
Google account
Python
Linux
Google Cloud Storage
To work on this project, you will need to create a google cloud account, you shouldn’t worry about cost as Google has $300 free credits for first time signups, which should be enough for the project. 
Go to Google Cloud account 
Create your project
Search for IAM > service account and create a user with storage objects admin and storage admin rights
NB: For company/commercial projects you should be careful about the rights you assign to a user.
Search for cloud storage and create a bucket for the project
Mage AI
We will be using the virtual environment setups for our project but you can also use the other two options.
Link to GitHub.
Create a virtual environment: python -m venv your-project-folder
Cd your-project-folder
Pip Install mage ai[google-cloud-storage]
Mage start your your-project-name

Project:
Use standard batch: loader 
Input the api URL to the URL open space and run the api
Transform: format the date using the transform format option.
In the transform block input the Date column as the column to be transformed.

Load: use the load option python to google cloud storage:
Input the bucket name and the name of the file to be used during loading into google cloud storage.
Open the io_config.yaml and input the key you created during iam role.
Give the file path in the google file path and comment the other parts of the google cloud requirements 
After this check the data loaded in the google cloud storage
You can set ups triggers for the pipeline to run on a schedule.
That’s it for now!!
