# SageMaker Deployment Project

This project builds a simple web app which interacts with a deployed recurrent neural network performing sentiment analysis on movie reviews. This project assumes some familiarity with [SageMaker](https://aws.amazon.com/sagemaker/).

## Final Web App
![A positive review](https://github.com/aaakashkumar/Sentiment-Analysis-Web-App/raw/master/screenshots/Screenshot%20from%202020-08-25%2000-12-23.png)
![A negative review](https://github.com/aaakashkumar/Sentiment-Analysis-Web-App/raw/master/screenshots/Screenshot%20from%202020-08-25%2000-12-11.png)

## Setup Instructions

The notebooks provided in this repository are intended to be executed using Amazon's SageMaker platform. The following is a brief set of instructions on setting up a managed notebook instance using SageMaker, from which the notebooks can be completed and run.

### Log in to the AWS console and create a notebook instance

Log in to the AWS console and go to the SageMaker dashboard. Click on 'Create notebook instance'. The notebook name can be anything and using ml.t2.medium is a good idea as it is covered under the free tier. For the role, creating a new role works fine. Using the default options is also okay. Important to note that you need the notebook instance to have access to S3 resources, which it does by default. In particular, any S3 bucket or object with sagemaker in the name is available to the notebook.

### Use git to clone the repository into the notebook instance

Once the instance has been started and is accessible, click on 'open' to get the Jupyter notebook main page. We will begin by cloning the SageMaker Deployment github repository into the notebook instance. Note that we want to make sure to clone this into the appropriate directory so that the data will be preserved between sessions.

Click on the 'new' dropdown menu and select 'terminal'. By default, the working directory of the terminal instance is the home directory, however, the Jupyter notebook hub's root directory is under 'SageMaker'. Enter the appropriate directory and clone the repository as follows.

```bash
cd SageMaker
git clone https://github.com/aaakashkumar/Sentiment-Analysis-Web-App.git
exit
```

After you have finished, close the terminal window.

### Open and run the notebook

Now that the repository has been cloned into the notebook instance you may open the `SageMaker Project.ipynb` notebook and run through its cells. Any additional instructions are contained in the notebook.

---

> This project was submitted as a part of the Machine Learning Engineering Nanodegree Program at Udacity
