# Career Levels Classification
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)

## About

Given the attributes for each job i expect a classifier that finds the correct career_levels. 

Possible career_levels:
  1. graduate_trainee
  2. specialist
  3. senior_specialist_or_project_manager
  4. manager_team_leader
  5. senior_manager_head_of_department
  6. director_bussiness_unit_leader
  7. managing_director_small_medium_company
  8. managing_director_large_company

## Dataset
Dataset: [Download career_levels.ods](https://github.com/tranvietcuong03/career_levels_prediction/blob/master/career_levels.ods) <br>
It will be this: 
|   |  Title                                            | Location      | description                                       | function	                               | industry	| career_level
|---|---------------------------------------------------|---------------|---------------------------------------------------|------------------------------------------|-----------|-------------|
| 1 | Cnslt - Systems Eng- Midrange 1                   | Seattle, WA   |Participates in design, development and implem...	|information_technology_telecommunications |Financial Services| senior_specialist_or_project_manager |
| 2 | SharePoint Developers and Solution Architects     | Dallas, TX    |We are currently in need of Developers who can...  |consulting                                |IT Consulting| senior_specialist_or_project_manager|
| 3 | Business Information Services - Strategic Acco... | North Carolina|Experian is seeking an experienced Account Exe...  |sales                                     |Security, Risk, Restructuring Consulting | senior_specialist_or_project_manager|
| 4 | Strategic Development Director (procurement)	    | Austin, TX    |Â Want to join a world-class global procuremen...  |procurement_materials_logistics           |Information Technology| bereichsleiter|


## Data Preprocessing
* Cleaning: Handled missing values and outliers.
* Normalize pattern: Used Regex to filter values
* Feature Engineering: Used RandomOverSampler to make a balance-data

## Setup
- Requirement: Ensure you have Python 3 and required libraries installed (pandas, numpy, sklearn, imblearn).
- Installation:
  * Pandas
  ```sh
  pip install pandas
  ```
   * Odf (It supports to read an excel file):
  ```sh
  pip install odfpy
  ```
  There are similar to numpy, scikit-learn and imblearn to install
  
## Model

I used **RandomizedSearchCV** for training the model to find the best results. I handled the text data using **TfidfVectorizer** and **OneHotEncoder**.


## Result:
* Accuracy: 0.71
* Precision: 0.63(macro avg), 0.70(weighted avg).
* Recall: 0.45(macro avg), 0.71(weighted avg).
* F1-score: 0.50(macro avg), 0.70(weighted avg).
