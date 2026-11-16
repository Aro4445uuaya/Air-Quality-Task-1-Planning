# Air Quality Sensor Data Engineering – Task 1

## 1. Project Overview

This project is developed as part of the Sensor Data Engineering Internship.

The objective is to study an air-quality sensor dataset, understand its structure, identify data-quality issues, and establish a structured approach for processing and managing sensor data.

This task focuses on data source research, initial dataset exploration, project planning, and understanding professional data engineering practices.

## 2. Data Source

**Dataset:** Air Quality Dataset

**Source:** UCI Machine Learning Repository

**Dataset Link:** https://archive.ics.uci.edu/dataset/360/air+quality

The dataset contains historical air-quality measurements collected using gas sensors and reference measurement instruments.

It includes the following measurements:

- Carbon Monoxide (CO)
- Non-Methane Hydrocarbons (NMHC)
- Benzene (C6H6)
- Nitrogen Oxides (NOx)
- Nitrogen Dioxide (NO2)
- Temperature
- Relative Humidity
- Absolute Humidity

## 3. Technologies Used

| Technology | Purpose |
|---|---|
| Python | Data processing |
| Pandas | Data analysis and transformation |
| NumPy | Numerical operations |
| MySQL | Planned data storage |
| SQLAlchemy | Planned database connectivity |
| Git | Version control |
| GitHub | Source code management |

## 4. Project Structure

```text
Air-Quality-Task-1-Planning/
│
├── src/
│   ├── inspect_data.py
│   ├── profile_data.py
│   ├── validate_datetime.py
│   ├── check_time_gaps.py
│   ├── check_sensor_values.py
│   └── data_quality_report.py
│
├── requirements.txt
├── README.md

```

## 5. Initial Data Exploration

The dataset was inspected using Python and Pandas.

Initial observations:

- Non-empty records analysed: 9,357
- Columns identified: 15
- Completely empty rows identified and removed: 114
- Duplicate rows detected: 0
- Invalid timestamps detected: 0
- Duplicate timestamps detected: 0

## 6. Data Quality Observations

The dataset uses `-200` as a missing-value marker in several sensor measurement columns.

The marker was converted into Pandas missing values (`NaN`) for further analysis.

Important observations:

- NMHC(GT) contains approximately 90.23% missing values.
- CO(GT) contains approximately 17.99% missing values.
- Several other sensor columns contain approximately 3.91% missing values.

Timestamp validation and hourly interval checks were also performed.

## 7. Python Scripts

| File | Description |
|---|---|
| inspect_data.py | Inspects dataset structure |
| profile_data.py | Analyses missing values and duplicates |
| validate_datetime.py | Validates timestamps |
| check_time_gaps.py | Checks hourly time intervals |
| check_sensor_values.py | Inspects sensor measurement ranges |
| data_quality_report.py | Generates a data-quality report |

## 8. Proposed Engineering Workflow

```text
Air Quality Dataset
        |
        v
Data Extraction
        |
        v
Data Profiling
        |
        v
Data Cleaning
        |
        v
Data Quality Validation
        |
        v
MySQL Data