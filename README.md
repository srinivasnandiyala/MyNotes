opendatasets is a Python library for downloading datasets from online sources like Kaggle and Google Drive using a simple Python command.


Installation
Install the library using pip:


pip install opendatasets --upgrade
Usage - Downloading a dataset
Datasets can be downloaded within a Jupyter notebook or Python script using the opendatasets.download helper function. Here's some sample code for downloading the US Elections Dataset:


import opendatasets as od
dataset_url = 'https://www.kaggle.com/tunguz/us-elections-dataset'
od.download('https://www.kaggle.com/tunguz/us-elections-dataset')
dataset_url can also point to a public Google Drive link or a raw file URL.

Kaggle Credentials
opendatasets uses the Kaggle Official API for donwloading dataset from Kaggle. Follow these steps to find your API credentials:

Go to https://kaggle.com/me/account (sign in if required).

Scroll down to the "API" section and click "Create New API Token". This will download a file kaggle.json with the following contents:

{"username":"YOUR_KAGGLE_USERNAME","key":"YOUR_KAGGLE_KEY"}
When you run opendatsets.download, you will be asked to enter your username & Kaggle API, which you can get from the file downloaded in step 2.
Note that you need to download the kaggle.json file only once. You can also place the kaggle.json file in the same directory as the Jupyter notebook, and the credentials will be read automatically.

IMPORTANT NOTE: If you're downloading a competition dataset, make sure to first accept the rules of the competition.
