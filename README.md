# Bash, Git, Hyperparameter Tuning and Logging Experiments

This week we are going to learn about a few ideas that will allow you to execute the development part of your thesis projects more successful. We are going to learn to about a few tools, namely, 

- Bash commands
- Git commands
- Doing hyperparameter tuning
- Logging relevant information when training models

## Learning Goals

There are several learning goals behind this week's exercise. You will familiarise with how to:


- Use [github](https://github.com/) to manage your code
- Use `bash` commands and `git` commands to add new changes to your code while keeping track of them. 
- Training a machine learning model in your personal computer
- Adding *hyperparameter tuning* to your code
- Logging the hyperparameters and metrics to track your experimental settings. 


## Exercise Plan

Today's exercise consists of several steps that need to be executed sequencially to obtain the final code that will conduct hyperparamter tuning for your machine learning model. 

- Step 1: Forking a public github repository to your own git profile
- Step 2: Pulling the git repository to your local environment
- Step 3: Do the instructed changes to your code to introduce hyperparameter tuning
- Step 4: Add logging to record the hyperparamters and the metrics 
- Step 5: Commit the changes and push them to a remote git repository. 
- Step 6: Submit a pull request


## Step 1: Forking a public github repository to your own git profile

- Sign into your [github account](https://github.com/) or register with github over [here](https://github.com/signup) 
- Fork the tutorial code found [here](https://github.com/comp0190/git_tutorial) to create your own version of the repository.


## Step 2: Pulling the git repository to your local environment

- Firstly, install Git on your local machine. You can find instructions for doing this [here](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).
- Then go to your desire folder and create a directory named `hyperparameter_tuning_tutorial` using *bash* commands. 
- Use the relevant git command to `clone` the repository into the directory you just created. 
- Finally, create a ***new branch*** named `hyperparams_and_logging` from the `master` branch of your repository before doing changes to the code. 

## Step 3: Do the instructed changes to your code to introduce hyperparameter tuning

- Open this notebook using the Jupyter notebook software. 
- Instructions on installing Anaconda that contains Jupyter notebook editor is found [here](https://docs.anaconda.com/anaconda/install/index.html)

### Importing Relevant Python Modules

There are several Python modules that we we aim to use today. Let us import them here. We use numpy and pandas for data manipulation. We use scikit learn for splitting data into train and test splits and implement grid search. We use xgboost to implement the desired machine learning model. We use logging library to log information. 

***Hint:*** You may use the `pip` python package manager to install these libraries in your local python environment. 

```
pip install numpy
pip install pandas
pip install scikit-learn
pip install xgboost
```

## Step 4: Add logging to record the hyperparamters and the metrics 

- Instead of printing the best set of hyperparameter values, use logging to add log messages that can capture these values. 

## Step 5: Commit the changes and push them to a remote git repository. 

- Use the relevant git command to *commit* the code into the local version of your repository
- Use the relevant git command to *push* the committed code into the `hyperparams_and_logging` branch of the remote repository (in github)

## Step 6: Submit a pull request

- Use the github web user interface to submit a ***pull request*** to your repository. Details found [here](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)  

***Hint:*** Details about pushing the new code to the branch is also found [here](https://comp0190.github.io/lectures/topics/3_tuning/git.html)