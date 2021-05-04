# Github Issue Classification

Towards automatically labelling issues reported on github.


## Fetching Data
This focus of this work was more recent data, as opposed to old datasets that are already [available on Google's BigQuery](https://console.cloud.google.com/marketplace/details/github/github-repos?filter=solution-type:dataset), [Kaggle](https://www.kaggle.com/davidshinn/github-issues) and various other internet sources.

Therefore, the first and foremost task was to systematically collect data from github.
For this purpose, we used nothing but github's own api. (Refer to Fetch Repos and Fetch Issues)

Furthermore, all the data that was collected has also been uploaded to public sources to facilitate future research and projects.

Repositories fetched from github associated with [IEEE's top 50 programming languages](https://ieeexplore.ieee.org/document/91505500 can be found at [Kaggle - Repositories dataset](https://www.kaggle.com/ansnadeem/github-repositories-of-top-50-languages)

The original issue dataset(s) can be found at [Kaggle - Issue Dataset](https://kaggle.com/ansnadeem/github-top-repository-issues)
The above kaggle link is associated with two datasets:-
1. issues.csv - Raw issue data extracted from top 50 repositories
1. labelled_issues_with_language.csv - Labelled data from the above dataset, also includes an identifier of the language that was used 

## Pre-processing Data for Training
[todo]

## License
[MIT License](https://github.com/ansnadeem/gh-issue-classification/LICENSE)
