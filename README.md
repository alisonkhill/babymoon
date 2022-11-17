# Babymoons

## Summary
This repo is intended to fulfill the project requirements for the Code Louisville Data Analysis 2 Class.

This project was inspired after seeing another Code Louisville student's project investigating whether there are more of certain types of injuries leading to emergency room visits on the full moon. She chose to investigate this because of the conventional wisdom that people tend to behave with less inhibitions when there is a full moon. I really enjoy data analyses that look at conventional wisdom to see if it holds water, and this project reminded me that I once heard a labor and delivery nurse claim that more babies are born on the full moon. I chose to investigate this using two Kaggle datasets:
- [fivethirtyeight births](https://www.kaggle.com/datasets/fivethirtyeight/fivethirtyeight-births-dataset)
- [full moon calendar](https://www.kaggle.com/datasets/lsind18/full-moon-calendar-1900-2050)

I chose a Juptyer notebook (.ipynb) format so I could inspect the results of my analysis as I went along and also to walk the viewer through the analysis. After importing 3 csv files and cleaning up the data, I was intially surprised to find that the births data was not normally distributed, but was bimodal instead. It turned out that there are more births on weekdays than weekends, and it was more useful to treat those two sets of data as separate groups. After splitting out weekdays and weekends, I compared the births on dates with a full moon against all other dates and found no significant difference.

A new hypothesis that arises from this analysis is that more babies are born on weekdays due to scheduled Cesarean sections and labor inductions. This represents and interesting future extension of this project, but is beyond the scope of the current analysis.

In summary: the data do not support the hypothesis that more babies are born on the full moon.

## Packages & Modules
Babymoons uses pandas, seaborn, datetime, and scipy.stats.

## Setup Instructions
Note: I recommend running this using Visual Studio Code if you want to inspect the dataframes and other variables. I used the Variables viewer to inspect my dataframes rather than displaying them inline to reduce space in the notebook. 

1. Run `git clone https://github.com/alisonkhill/babymoons.git` to clone this repo to your machine.

2. In the babymoons directory, set up a virtual environment:
    - On Mac/Linux:
        - open the Terminal and create a virtual environment with the command `python3 -m venv virtual-env`
        - activate the virtual environment with the command `source virtual-env/bin/activate`
    - On Windows, 
        - open the Command Prompt and create a virtual environment with the command `python -m venv virtual-env`
        - activate the virtual environment with the command `virtual-env\Scripts\activate.bat`

4. Install packages in the requirements.txt file: `pip install -r requirements.txt`

5. Finally, run `main.ipynb` or walk through the notebook step by step.

## Code Louisville Requirements

- [x] The project is uploaded to your GitHub repository and shows at minimum 5 separate commits.
- [x] The project includes a README file that explains the following:
    - A one-paragraph or longer description of what your project is about.
    - Relevant packages that need to be installed to run the project.
    - Which 5+ features you have included from the below lists to meet the requirements
    - Any special instructions are required for the reviewer to run your project. (For example: “run python main.py” from the command line)
- [x] The project implements a data analysis program that uses pandas, matplotlib, and/or numpy to perform an analysis project of 2 or more pieces of data and implement a rich data visualization in Tableau / Jupyter/Plotly/Matplotlib, or something similar. At a minimum, the program should ingest, analyze, and display data. Any needed data cleaning should be clearly documented and repeatable.

### Choose at least 1 item from each category on the Features List below and implement them in your project

#### Category 1: Loading Data
- [x] Read TWO data files (JSON, CSV, Excel, etc.). 

Three csvs are read for this project, obtained from the kaggle datasets mentioned above.

#### Category 2: Clean and operate on the data while combining them
- [x] Clean your data and perform a pandas merge with your two data sets, then calculate some new values based on the new data set. 

The data is cleaned in several ways, including removing whitespace, changing date data to datetime format. A pandas merge is used to combine birth and full moon data, and new columns with categorical variables are created.

#### Category 3: Visualize / Present your data
- [x] Make 3 matplotlib or seaborn (or another plotting library) visualizations to display your data.

Multiple seaborn plots are included as part of this project's analysis.

#### Category 4: Best Practices
- [x] Utilize a virtual environment and include instructions in your README on how the user should set one up

See requirements.txt file in repo.

#### Interpretation of your data:
- [x] Annotate your code with markdown cells in Jupyter Notebook, write clear code comments, and have a well-written README.md. Tidy up your notebook, and make sure you don’t have any empty cells or incomplete cells that don’t do anything. Make sure it’s all functional before your final github commit.

The project notebook contains markdown that outlines the steps and features of the project, as well as code comments to provide further context and rationale for why each step was completed.