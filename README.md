# Default Payments Classification Azure ML Example

This set of notebooks runs through 3 different areas of Azure Machine Learning Python SDK in a easy to understand step by step senario.  Given a labelled dataset (in this case default payment data) we will create an AutoML workspace, automatically build a high quality machine learning model, deploy the model to a azure container instance and then run predictions on a set of data files, outputing the result into a single CSV.

You can learn the basics of the AML Python SDK [here](https://github.com/Azure/MachineLearningNotebooks)

## 0_setup.ipynb - Create Azure Workspace
This notebook creates a Automated machine learning (automated ML) workspace that will amoung other things build high quality machine learning models for you by automating model and hyperparameter selection. This notebook will show you how to create a workspace and a seperate storeage account that will host our data. You can see how to upload data into a Datastore and share it by registering a Dataset.

## 1_build_model.ipynb - Build and Deploy the Best Model
This notebook will show you how to authenticate with the workspace we created in the 1st notebook and connect to the data with the Dataset that was previously registered. You can see how to create a compute cluster or use an existing one by name. You are then able to create a pandas dataframe and analyse the data. Next, you are shown how to use AutoML to to build and test the best model. Finally you will see how you can deploy this model to an azure container instance.

## 2_test_model_webservice.ipynb - Predict with the Model
In this notebook you will see how you can connect to the workspace and the DataStore, then load data to predict into a dataframe. The data is then looped through to determine scores per line item using the webservice. The result is filtered for only bad predicted default payments and written to a CSV file.
