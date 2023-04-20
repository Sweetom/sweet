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

The objective of the project is to build a model to predict life expectancy of a population.  This will help with assessing the factors that affect longevity.  For instance, looking at the data provided we can observe that some diseases are related to the cause of declining life expectancy. Therefore, knowing the core of the problem allows an organization such as Centers for Disease Control and Prevention (CDC) determine what vaccinations are important and also propose possible prevention measures. 

Therefore, to answer some of the questions, I have decided to build two prediction models and compare each on performance level to be utilized in the organization. The first model that was created was **Multiple Regression Model**. I chose this model to assess the relationship between the different variables and the target variable. The reason I chose this model is due to its easier interpretability and usefulness in detecting significant variables that help to determine life expectancy. 

The other model that is being utilized in this project is **Lasso Regression Model**. This model would be beneficial in obtaining enhanced prediction accuracy. In addition to its ability to conduct feature selection. This choice of model was made given our objective of the project which is to assess the factors that affect life expectancy. Therefore, it would be a valuable model to the organization.

During the exploratory data analysis, I observed that some of the features were highly correlated. A heat map was used to detect correlation between some variables, and some of the highly correlated variables were GPD and percentage expenditure as well as under five deaths and infant deaths. Hence, the model choice of Lasso was based on that. Lasso reduces multicollinearity by shrinking the coefficients of the features that demonstrate multicollinearity. Additionally, one of the important observations was that an average of 79 years was a life expectancy in the developed countries which was 12 years more than the developing countries that had an average of 67 years. As a result, this gap between the two would lead us to assume that in developed countries the necessary resources are readily available to aid in longer life spans. Some of the variables that were directly associated with *Life Expectancy* were *Adult Mortality* and *HIV/Aids* which were negative, and the relationship was that as each variable increase, life expectancy decreases. The ones that had strong positive correlation were *Income composition of resources* and *Schooling*. This indicates that as each variable increases, life expectancy also increases. To summarize, these features are some important factors that affect life expectancy. However, we will use the models to solidify our findings.

After building both the Multiple Regression and Lasso models, I have found that the latter is more explainable. Both models have demonstrated high prediction accuracy scores with small number of errors which is the main goal when building a regression model. Nonetheless, Lasso regression model provides a less complicated and concise results that can be easily explained and comprehended. When fitting the data and obtaining the result, Lasso aims to perform feature selection by shrinking the coefficients to zero for the less contributing features. Therefore, distinguishing between them becomes easy and consequently, making the model more explainable. Whereas multiple regression model, would be a little complex to explain to a non-technical individual as one would have to explain the importance of the p-value and how it is assessed overall.

It is important not to confuse a lay audience with technical concepts when communicating ideas. Most importantly, it is vital to include most of the details, however, effectively relaying the message in a practical way can be somewhat challenging. The approach to explaining the techniques and the output is to omit the technical vocabulary and deliver it in a coherent way. We want to tell a story with the data that we have obtained. For instance, I would not include the data cleaning and preprocessing, but we would include what data we are using to assess the relationship between the variables and the target variable. In this case, explaining what factors we need to include to predict or to understand what affects life expectancy, and how to solve the problem would be a good start. One way is to incorporate visualizations to capture everyone’s attention and aid in storytelling. 

Executive teams would want to understand the business impact of machine learning models and their techniques. Therefore, I would explain the business objective and reliability of the model in tackling the issue at hand. In assessing the model’s accuracy, I have used metrics such as R-squared, Root Mean Squared Error etc. However, since it is good practice to avoid using those technical details when explaining it to lay audience or executive team; instead, I would elaborate that we have tested the model for accuracy, and it shows 82% accuracy in predicting life expectancy and shows less error which is an indicator of a good model. 



# Data Source
https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who