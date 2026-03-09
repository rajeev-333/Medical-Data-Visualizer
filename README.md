# Medical Data Visualizer

A Python project built as part of the **FreeCodeCamp Data Analysis with Python** certification.

## Description
Visualizes and analyzes medical examination data using **Matplotlib**, **Seaborn**,
and **Pandas**. The dataset contains patient body measurements, blood test results,
and lifestyle choices collected during medical examinations. The project explores
the relationship between cardiac disease, body measurements, blood markers, and
lifestyle choices.

## Visualizations Produced

### 1. Categorical Plot (`catplot.png`)
Shows the count of good (0) and bad (1) outcomes for the following features,
split by patients with and without cardiovascular disease (`cardio = 0` and `cardio = 1`):
- Cholesterol
- Glucose
- Smoking
- Alcohol intake
- Physical activity
- Overweight status (BMI-based)

### 2. Correlation Heatmap (`heatmap.png`)
Displays the correlation matrix of all medical features after cleaning the dataset
by removing patients with invalid/outlier measurements.

## Data Cleaning Applied
- Removed patients where diastolic pressure > systolic pressure
- Removed height values below 2.5th percentile and above 97.5th percentile
- Removed weight values below 2.5th percentile and above 97.5th percentile

## How to Run

### Install dependencies
```bash
pip install matplotlib seaborn pandas numpy
```
### Run the project
```bash
python main.py
```
## Project Structure
```
├── medical_data_visualizer.py  # Main solution file
├── medical_examination.csv     # Medical dataset
├── main.py                     # Run and test the solution
├── test_module.py              # Unit tests (do not modify)
├── examples/
│   └── Figure_1.png            # Reference chart
|   └── Figure_2.png            # Reference chart
├── catplot.png                 # Generated categorical plot
├── heatmap.png                 # Generated correlation heatmap
└── README.md
```

## Dataset Description
```
| Feature                  | Variable    | Type                                             |
| ------------------------ | ----------- | ------------------------------------------------ |
| Age                      | age         | int (days)                                       |
| Height                   | height      | int (cm)                                         |
| Weight                   | weight      | float (kg)                                       |
| Gender                   | gender      | categorical code                                 |
| Systolic blood pressure  | ap_hi       | int                                              |
| Diastolic blood pressure | ap_lo       | int                                              |
| Cholesterol              | cholesterol | 1: normal, 2: above normal, 3: well above normal |
| Glucose                  | gluc        | 1: normal, 2: above normal, 3: well above normal |
| Smoking                  | smoke       | binary                                           |
| Alcohol intake           | alco        | binary                                           |
| Physical activity        | active      | binary                                           |
| Cardiovascular disease   | cardio      | binary (target)                                  |
```
## Technologies Used
* Python 3

* Pandas

* NumPy

* Matplotlib

* Seaborn
