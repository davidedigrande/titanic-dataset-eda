# Exploratory Analysis of the Titanic Dataset

The sinking of the Titanic is one of the most famous shipwrecks in history. On April 15, 1912, during its maiden voyage, the Titanic sank after colliding with an iceberg, causing the death of 1502 of the 2224 passengers and crew members. The construction of the Titanic cost about 7.5 million dollars, and it sank into the ocean due to the collision.

Dataset: [Titanic - Kaggle](https://www.kaggle.com/competitions/titanic)

## Objective
The goal is to create a notebook for conducting an exploratory data analysis to determine if the survivors were simply lucky or if some individuals had a higher chance of surviving based on their characteristics.

For this project, we will use the `pandas` library for data manipulation and `matplotlib` for data visualization.

## Analysis Steps

#### 1. Importing the Dataset
Import the dataset using `pandas` and display the table.

#### 2. Exploring Missing Values
Examine the missing values in the dataset.

#### 3. Feature Analysis
- What are the Categorical features?
- What are the Ordinal features?
- What are the Continuous features?

#### 4. Survived
What type of variable is it?
Number of survivors: this is the variable we are interested in exploring and understanding, while we will explore all the other features in relation to it. Let's start by creating some charts on the number of survivors (such as Pie or Bar charts).

#### 5. Sex (Gender)
- What type of variable is it?
- How many men and women survived? And how many did not?
- Choose a visualization to best summarize the information.
- **What insights can we derive?**

#### 6. Pclass (Ticket Class)
- What type of variable is it?
- How are the different classes divided between survivors and non-survivors? Is there a relationship between the wealth of passengers and their probability of survival?
- Choose a visualization to best summarize the information.
- **What insights can we derive?**

#### 7. Relationship between Sex and Pclass
Does class influence the chances of survival more for one gender than the other, or does it not make a difference? Hint: a visualization that allows distinguishing three dimensions might be a good choice here.

#### 8. Age
- What type of variable is it?
- Describe the distribution: find the minimum, maximum, mean, median, and mode.

  ##### Data Cleaning and Feature Extraction
  Let's study the variable further to improve data quality:
  - **Missing Values:**
    - How many missing values are there?
    - What general approaches can we use to impute missing values? What could be the problem with a generic approach in this case?
  - **Feature Extraction:**
    - For this dataset, we can use a specific approach: the `Name` column also contains the title (Master, Miss, Mr, Mrs). Perform feature extraction by creating a new column from the name column, containing only the title.
    - To achieve this, use the following regex: `'([A-Za-z]+)\.'`.
    - Once the title column is obtained, compute the average age for each title and impute missing age values based on this result.

#### 9. Relationship between Sex, Pclass, and Age:
  - How does age relate to class? And to gender? Hint: creating two visualizations that allow distinguishing three dimensions (age, gender or class, survival) might be a good choice here.
  - **What insights can we derive about the survival of different demographics?**

#### 10. Correlations between Features (Pearson's Linear Correlation)
- Create a correlation heatmap between the features.
- **What insights can we derive from this heatmap?**

#### 11. Summary of Findings for Each Feature
- Summary of observations and insights for each analyzed feature.
