# Pattern recognition and machine learning exercises

Python scripts for the lab exercises, quizzes and midterms of a university pattern recognition and machine learning course: classification, dimensionality reduction and clustering with scikit-learn and pandas.

## Context

Pattern Recognition and Machine Learning at the Aristotle University of Thessaloniki, School of Electrical and Computer Engineering, academic year 2021-22. Individual work.

The course had a lecture and a lab session every week. In each lab session an assistant went through a Python script and explained the theory behind it. After each lab a quiz with a similar task was solved individually, and there were two midterms.

- The lab scripts (`labs/`) are based on the code of the course's lab handouts, which was worked through in the lab sessions. They are not original work.
- The quiz scripts (`quizzes/`) and the midterm scripts (`midterms/`) are solutions to the individual quiz tasks and to the two midterms.
- The datasets in this repo were issued by the course.

The questions of the quizzes and midterms are not included: the first line of each script says what it computes.

## What is in it

| Folder | Topic |
|---|---|
| `labs/01-introduction-to-python` | Python and pandas basics: lists, dataframes, reading files, missing values, one-hot encoding |
| `labs/02-decision-trees` | Gini index and information gain computed by hand, decision trees with scikit-learn, plotted and printed as text |
| `labs/03-naive-bayes` | Categorical naive Bayes with and without smoothing, Gaussian naive Bayes with accuracy, precision, recall, F1 and a ROC curve |
| `labs/04-ann` | A neural network regressor (`MLPRegressor`) with a train and test split and its error |
| `labs/05-knn-svm` | k-nearest neighbours and support vector machines, with 10-fold cross-validation to choose the RBF kernel parameter |
| `labs/06-preprocessing-pca-isomap` | Standardisation, PCA with eigenvalues and information loss, ISOMAP |
| `labs/07-kmeans` | k-means with chosen starting centres, inertia, a separation measure, silhouette plots, k-medoids |
| `labs/08-hierarchical-clustering-dbscan` | Agglomerative clustering with dendrograms and silhouette, DBSCAN, a k-means comparison |
| `labs/09-expectation-maximization-gmms` | A hand-written EM loop for a Gaussian mixture, scikit-learn's `GaussianMixture`, AIC and BIC |
| `quizzes` | Ten quiz scripts: descriptive statistics, Gini, ROC and AUC, MLP error, k-NN, SVM, PCA with k-NN, k-means, clustering, Gaussian mixtures |
| `midterms` | Three midterm solutions: classification on a traffic-severity dataset, k-means on a country dataset, PCA with hierarchical clustering |

Each script reads its data from its own folder, so run it from there.

## Getting started

### Requirements

Python 3.12 with the packages in `requirements.txt` (numpy 1.26.4, pandas 2.2.3, scipy 1.13.1, scikit-learn 1.5.2, matplotlib 3.9.2, seaborn 0.13.2, yellowbrick 1.5, scikit-learn-extra 0.3.0, setuptools). Newer releases of numpy and scikit-learn break lab 7, so the versions are pinned.

### Run

```
python -m venv .venv
.venv\Scripts\activate          # on Linux or macOS: source .venv/bin/activate
pip install -r requirements.txt
cd labs/05-knn-svm
python knn-svm.py
```

Most scripts open figure windows and wait for each to be closed.

## Project structure

```
labs/                 01-introduction-to-python/ ... 09-expectation-maximization-gmms/:
                      one script per lab, plus the lab's data files
                      (02 also has lab2.py)
quizzes/              quiz1.py ... quiz9.py, quiz5-2.py, and the quiz data (CSV)
midterms/             midterm1-groupa-part1.py, midterm2-groupa-part1.py,
                      midterm2-problem.py, and their data (CSV)
requirements.txt
```

In the midterm file names, "groupa" is the exam version, not a work group.

## Limitations

- Run and checked only on Windows 11 with Python 3.12.2, without a display: the figures were not looked at and the scripts were not tried with an interactive plot window.
- The quiz and midterm outputs were not checked against expected answers (none are included), and part of `midterm2-groupa-part1.py` is commented out.
- Lab 7 needs yellowbrick and scikit-learn-extra, which do not work with the newest scikit-learn and numpy 2.
- The scripts are exercise code, not a library: they print and plot results and are meant to be run one at a time.

## Credits and licence

The code is under the MIT licence (see `LICENSE`). The lab scripts in `labs/` are based on the course's lab handouts: the licence covers the changes made to them, not the handout code. It covers the quiz and midterm solutions. The data files (the `.txt` files in the lab folders and all `.csv` files) were issued by the course and are not covered by the licence.
