# Vehicle Defect Component Analysis

This is a university group project where we worked with several vehicle-related datasets and tried to find out which defective components appeared most often in different German cities.

The main idea was to combine data from vehicles, registrations, components, spare parts, and defect records. After cleaning and filtering the data, we created a final table showing the number of defective motors, transmissions, and seats for each selected city.

## What this project is about

In this case study, the data was split across many CSV files instead of being in one simple table. Because of that, a big part of the work was understanding how the files were connected and how to merge them correctly.

We focused on vehicles that were marked as defective and registered between 2014 and 2016. Then we looked at selected German cities and checked which major components were connected to the defective vehicles.

The cities included in the final analysis were:

- Augsburg
- Ingolstadt
- Regensburg
- Würzburg
- Bamberg
- Bayreuth
- Aschaffenburg
- Erlangen
- Rosenheim
- Landshut

## Files in this repository

```text
vehicle-defect-component-analysis/
│
├── README.md
├── notebooks/
│   ├── case_study.ipynb
│   └── general_tasks.ipynb
│
└── data/
    └── Final_dataset.csv
```

The two notebooks contain the main work from the project:

- `case_study.ipynb` contains the main case study analysis and the final component defect summary.
- `general_tasks.ipynb` contains additional tasks from the course, including delay analysis, regression, and other smaller data analysis questions.
- `Final_dataset.csv` is the final processed dataset created from the case study.

## Tools used

- Python
- Jupyter Notebook
- pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly
- SciPy
- scikit-learn
- statsmodels

## What was done

### 1. Loaded and cleaned the data

The original data came from different CSV files. Some files had different formats and separators, so we first had to load them correctly and clean them before starting the analysis.

Some of the cleaning steps included:

- removing unnecessary index columns
- checking missing values and duplicates
- converting date columns
- filtering the data to the required years
- making the datasets easier to merge

### 2. Found defective vehicles

We combined different vehicle datasets and filtered the records to keep only vehicles that were marked as defective. We also used registration data to connect the defective vehicles to their cities.

### 3. Connected vehicles to components

After finding the defective vehicles, we joined them with the component data. This helped us see whether the defect was related to components such as:

- motor
- transmission
- seats
- bodywork

For the final result, we focused mainly on motor, transmission, and seat defects.

### 4. Created the final city summary

At the end, we grouped the results by city and created a final dataset showing the number of defective motors, transmissions, and seats for each selected city.

## Final result

| City | Defective Motors | Defective Transmissions | Defective Seats |
|---|---:|---:|---:|
| Aschaffenburg | 8 | 5 | 1 |
| Augsburg | 33 | 14 | 5 |
| Bamberg | 12 | 6 | 3 |
| Bayreuth | 10 | 4 | 1 |
| Erlangen | 13 | 6 | 3 |
| Ingolstadt | 15 | 8 | 2 |
| Landshut | 10 | 7 | 2 |
| Regensburg | 15 | 8 | 3 |
| Rosenheim | 9 | 5 | 1 |
| Würzburg | 18 | 8 | 2 |

From the final table, Augsburg had the highest number of defective components in all three categories. Motor defects were also the most common type of defect overall, while seat defects were much lower compared to motors and transmissions.

## Other analysis in the project

The second notebook includes some extra tasks from the course, such as:

- checking logistics delay times
- calculating average delay using working days
- creating visualizations
- explaining relational data storage
- using linear regression for mileage analysis
- identifying possible hit-and-run vehicles based on the available data

## Note

This project was completed as part of a university group assignment. The repository includes the notebooks and final processed dataset, but not all original raw CSV files used during the course.
