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

https://alida.tistory.com/69

3c
reprojection error
he re-projection error corresponds to the image distance between a projected point and a measured point, and is used to quantify how closely the estimate of a 3D point recreates the true projection [13]. The projection error cost function through bundle adjustment is shown in Equation 20.

ORB-SLAM (Oriented FAST and Rotated BRIEF Simultaneous Localization and Mapping) is a feature-based monocular SLAM system that employs outlier rejection techniques to improve the robustness of its tracking algorithm. The two primary techniques used for outlier rejection in ORB-SLAM are reprojection error and RANSAC (Random Sample Consensus). These techniques are used to reject outliers in the feature matching process, which helps to ensure that the system only uses reliable correspondences to estimate the camera pose and map structure.
    1. Reprojection Error:
Reprojection error is the difference between the observed feature location in the image and the projected location of the corresponding 3D point. For a given camera pose and 3D point, the reprojection error (e) can be computed as follows:
e = || x - K * (R * X + t) ||
where:
    • x is the observed 2D image point
    • K is the camera's intrinsic matrix
    • R is the rotation matrix of the camera pose
    • t is the translation vector of the camera pose
    • X is the 3D point in the world coordinate system
In ORB-SLAM, when matching features between the current frame and the local map, a threshold on the reprojection error is used to reject outliers. By keeping only matches with a low reprojection error, ORB-SLAM ensures that the resulting correspondences are more likely to be correct.
    2. RANSAC:
RANSAC is an iterative method for estimating a model's parameters from a set of data points that may contain outliers. In the context of ORB-SLAM, RANSAC is used to find a consistent set of feature correspondences between the current frame and the local map, and to estimate the camera pose.
The RANSAC algorithm for camera pose estimation in ORB-SLAM can be described as follows:
a. Randomly select a minimal subset of feature correspondences. b. Compute the camera pose (R, t) from the selected correspondences using a perspective-n-point (PnP) algorithm. c. Calculate the reprojection error for all correspondences using the estimated camera pose. d. Count the number of inliers (i.e., correspondences with a reprojection error below a predefined threshold). e. Repeat steps a-d for a predefined number of iterations. f. Choose the camera pose with the largest number of inliers.
By using RANSAC in conjunction with the reprojection error, ORB-SLAM is able to effectively reject outliers and obtain a reliable estimate of the camera pose, which is crucial for accurate and robust tracking in SLAM systems.

