# Economic Fluctuations and Job Satisfaction in Spain

## Project Introduction

This repository contains the data science project "How Economic Fluctuations Influence Job Satisfaction Among Employees in Spain". It utilizes data from the European Social Survey's 10th round (2020) to explore the relationships between economic conditions, job security, work-life balance, and their impacts on job satisfaction levels among Spanish employees.The focus of this project is to analyse How economic fluctuations influence job satisfaction among employees in Spain, considering the impact of job security and work-life balance. The target variable under analysis is ‘How satisfied are you in your main job’. The dependent variable uses a score from 0 to 10 with 0 being 'Extremely dissatisfied' and 10 being 'Extremely satisfied'. Since the focus of the project was Binary Regression, we transform our dependent using mean, and median (respectively) for the cutoff, to be binary: **satisfied and not satisfied.**

The methodology followed throughout the project respected the eight stages for building predictive econometric models, namely, Exploratory Data Analysis and Data Preparation, Creation of  a Richer Set of Covariates, Variable Selection, Multicollinearity Issue, Model Estimation, Model Validation, Model Selection and Interpretation and Prediction. The current report will carefully detail each of the previously mentioned steps in the context of the Spanish reality regarding job satisfaction.


## Dataset Overview

- **Full Dataset - Spain.csv & Full Dataset - Spain.html**: Initial datasets for variable selection.
- **Full Dataset - Spain - Variable Selection - Stage 1 - FINAL.xlsx**: Prepared dataset for model implementation, derived from the initial datasets.

## Project Structure

1. **01_Preliminary_Variable_Selection.ipynb**
   - Focuses on the preprocessing of raw data and selection of relevant variables.
2. **02_Data_Analysis_Modelling_Prediction.ipnyb**
   - Covers exploratory data analysis, model building, predictions and validation processes.

## Getting Started with Google Colab

Google Colab is a free, cloud-based service that allows you to run Jupyter Notebooks without any local setup. It's perfect for this project as it simplifies the process of running complex data analysis and model training sessions. Follow these steps to use Colab:

### Step 1: Access Google Colab

- Navigate to [Google Colab](https://colab.research.google.com/). Log in with your Google account if prompted.

### Step 2: Open Project Notebooks

- Once in Colab, click on `File` > `Open notebook`.
- Select the `GitHub` tab in the popup window.
- Enter the URL of this GitHub repository and press Enter.
- You will see a list of available Jupyter notebooks (`.ipynb` files) in the repository. Click on the one you wish to open.


### Step 3: Uploading Data Files

Some notebooks may require access to the dataset files listed in the Dataset Overview section. Follow these steps to upload data files to Colab:

- In the Colab notebook, click on the folder icon on the left sidebar to open the Files tab.
- Click on the upload icon (📤) and select the data files from your computer.
- For '01_Preliminary Variable Selection.ipynb' notebook, upload these files 'Full Dataset - Spain.csv' & 'Full Dataset - Spain.html'
- For '02_Data_Analysis_Modelling_Prediction.ipynb' notebook, upload 'Full Dataset - Spain - Variable Selection - Stage 1 - FINAL.xlsx'
- Wait for the upload to complete. You can then access these files from the notebook.

### Step 4: Running Notebooks

- After uploading the files, you can run the code cells sequentially by clicking on the play button (▶️) on the left side of each code cell.
- To run all cells in the notebook, you can go to `Runtime` > `Run all`.

## Analysis Phases

### Preliminary Variable Selection

- **Notebook**: `01_Preliminary_Variable_Selection.ipynb`
- **Objective**: To clean and select relevant variables from the raw dataset.
- **Key Steps**:
  1. Data cleaning, including handling missing values and renaming columns for clarity.
  2. Preliminary analysis to identify variables significantly impacting job satisfaction.

### Model Implementation

- **Notebook**: `02_Data_Analysis_Modelling_Prediction.ipynb`
- **Objective**: To build predictive models that assess the impact of various factors on job satisfaction.
- **Key Steps**:
  1. Exploratory Data Analysis (EDA) to understand data distribution and underlying patterns.
  2. Creation of a richer set of covariates, including handling multicollinearity and variable transformation.
  3. Model building, including Logistic Regression and Probit models, to estimate the influence of selected variables on job satisfaction.
  4. Model validation and selection based on performance metrics like AUC, R2 Efron, and classification accuracy.
 
### Model Generation and Selection

This phase of the project delves into the creation and comparative analysis of three distinct models aimed at understanding the impact of economic fluctuations on job satisfaction among employees in Spain. Each model approaches the dataset with a unique perspective, utilizing a mix of categorical variables, interaction variables, and original variables with transformations.

#### Model 1: Binned Model with Categorical Variables

- **Objective**: To capture patterns and relationships within the data using only categorical variables.
- **Methodology**: 
  - Binning of numeric and ordinal features.
  - Generation of dummy variables for binned features.
  - Selection of variables based on the Chi-Square test of independence.
  - Mitigation of multicollinearity through Spearman correlation coefficient and VIF analysis.
- **Estimation & Validation**:
  - Logistic regression model estimation.
  - Validation through convergence checks and information criteria (AIC, BIC, and Likelihood Ratio Test).

#### Model 2: Model with Interaction Variables

- **Objective**: To investigate the complex relationships contributing to job satisfaction through interaction variables.
- **Methodology**:
  - Enrichment of covariates with square, cube transformations, and two-level interaction effects.
  - Variable selection through Spearman rank correlation test for numeric and ordinal covariates and chi-squared test for nominal covariates.
  - Handling multicollinearity with a VIF threshold of 10.
- **Estimation & Validation**:
  - Estimation using the Probit model.
  - Validation shows higher information criteria values compared to Model 1, suggesting Model 1's superior fit.

#### Model 3: Model with Original Variables and Transformations

- **Objective**: To explore the impact of non-linear effects and transformations on the prediction of job satisfaction.
- **Methodology**:
  - Application of various transformations to numerical features.
  - Standardization of the dataset for consistent scale across features.
  - Reduced feature set based on Chi-square test of independence and VIF analysis.
- **Estimation & Validation**:
  - Logistic regression model estimation.
  - Higher information criteria values compared to Models 1 and 2, indicating Model 1 as the best fit among the three.

### Model Selection and Conclusion

The selection of the best model was based on a comprehensive evaluation involving AUC, R2 Efron, classification accuracy, and the analysis of prediction errors. Model 1 emerged as the optimal choice, demonstrating the highest AUC, better explanatory power, and superior classification accuracy.

### Key Insights

- Emotional attachment to the country, happiness levels, and support from line managers significantly influence job satisfaction.
- The binned approach of Model 1 effectively captures the nuances of job satisfaction dynamics, outperforming more complex models.

## Conclusion

The exploration of economic fluctuations on job satisfaction in Spain, leveraging data from the European Social Survey, has culminated in significant insights. The study underscored the importance of emotional well-being, workplace support, and socio-demographic factors in determining job satisfaction levels. Model 1, with its binned categorical approach, provided a robust framework for predicting job satisfaction, offering a foundation for targeted interventions aimed at enhancing employee well-being amidst economic changes.

## Contributing

We welcome contributions to improve the project. Please fork the repository, make your changes, and submit a pull request with a description of your modifications.

## Acknowledgments

- European Social Survey for the comprehensive data on Spain.
- Our professors and colleagues for their invaluable feedback and support throughout this project.

