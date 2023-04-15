Life Expectancy Project
==============================
#### Population Health Analysis
This model is utilized to analyze and understand the main factors that affects population health. The question we would try to answer is how an organization can promote public health by allocating the required resources such as health care system, coverage funding etc. This model will help in understanding the problem and making informed choices on the future of overall health. I will be using two models, **Multiple Regression** and **Lasso Regression**.


Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io

--------
# Project Description


<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>

The objective of the project is to build a model to predict life expectancy of a population.  This will help with assessing the factors that affect longevity.  For instance, looking at the data provided we can observe that some diseases are related to the cause of declining life expectancy. Therefore, knowing the core of the problem provides an organization such as Centers for Disease Control and Prevention (CDC) determine what vaccinations are important and also propose possible prevention measures. 

Therefore, to answer some of the questions, I have decided to build two prediction models and compare each on performance level to be utilized in the organization. The first model that was created is **Multiple Regression Model**. I chose this model to assess the relationship between the different variables and the target variable. The reason I chose this model is due to its easier interpretability and usefulness in detecting significant variables that helps to determine life expectancy. 

The other model that is being utilized in this project is **Lasso Regression Model**. This model would be beneficial in obtaining an enhanced prediction accuracy. In addition to its ability to conduct feature selection. This choice of model was made given our objective of the project which is to assess the factors that affect life expectancy. Therefore, it would a valuable model to the organization.

During the exploratory data analysis, I observed that some of the features were highly correlated. A heat map was used to detect correlation between some variables, and some of the high correlated variables were GPD and percentage expenditure as well as under five deaths and infant deaths. Hence, the model choice of Lasso was based on that. Lasso reduces multicollinearity by shrinking the coefficients of the features that demonstrates multicollinearity. Additionally, one of the important observations was that an average of 79 years was a life expectancy in the developed countries which was 12 years more than the developing countries that had an average of 67 years. As a result, this gap between the two would lead us to assume that in developed countries the necessary resources are readily available to aid in longer life span.  


# Data Source
https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who