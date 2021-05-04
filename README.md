# Github Issue Classification

Towards automatically labelling issues reported on github.

## Steps to run
1. Run Fetch Repositories notebook
2. Run Fetch Issues notebook

Step 1 and 2 can be skipped by downloading the datasets from the [kaggle](https://kaggle.com/ansnadeem) links below, and placing them in the directory of the training notebook.

3. Run the Cleaning and training notebook (To run this notebook faster, also download the labelled_issues_with_language.csv from below)


## Fetching Data
This focus of this work was more recent data, as opposed to old datasets that are already [available on Google's BigQuery](https://console.cloud.google.com/marketplace/details/github/github-repos?filter=solution-type:dataset), [Kaggle](https://www.kaggle.com/davidshinn/github-issues) and various other internet sources.

Therefore, the first and foremost task was to systematically collect data from github.
For this purpose, we used nothing but github's own api. (Refer to Fetch Repos and Fetch Issues)

Furthermore, all the data that was collected has also been uploaded to public sources to facilitate future research and projects.

Repositories fetched from github associated with [The top programming languages](https://ieeexplore.ieee.org/document/91505500) can be found at [Kaggle - Repositories dataset](https://www.kaggle.com/ansnadeem/github-repositories-of-top-50-languages)

The original issue dataset(s) can be found at [Kaggle - Issue Dataset](https://kaggle.com/ansnadeem/github-top-repository-issues)
The above kaggle link is associated with two datasets:-
1. issues.csv - Raw issue data extracted from top 50 repositories
1. labelled_issues_with_language.csv - Labelled data from the above dataset, also includes an identifier of the language that was used 

## Pre-processing Data for Training
This part involves a number of steps. At first we observe that the dataset contains almost 48% labelled issues. Which means that 52% of the issues are not labelled, which is the problem that we intend to solve.
Then out of the labelled data, we filter out results that are only in english language.
Finally, we pre-process data and add appropriate columns and values to make it a multi-class problem. Moreover, we only classify for default github labels that correspond to maintainence activities such as feature, bug, and enhancement.

## Training
In the training phase we fit three models
* Naive Bayes - as a baseline model
* Logistic Regression
* LinearSVC.


## Evaluation
We compare the acuracy of all the models and find that LinearSVC performs the bset.


## License
[MIT License](https://github.com/ansnadeem/gh-issue-classification/LICENSE)
