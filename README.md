# NYC Schools SAT Analysis

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python) ![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas) ![Plotly](https://img.shields.io/badge/Plotly-Interactive%20Viz-3F4F75?logo=plotly) ![DataCamp](https://img.shields.io/badge/DataCamp-Course%20Project-03EF62?logo=datacamp)

## Project Overview

This project analyzes SAT performance data from New York City public high schools. Using publicly available standardized test results, the analysis identifies high-performing schools, compares institutions on the basis of combined SAT scores, and examines borough-level variation in academic outcomes. The goal is to derive meaningful, data-driven insights into educational performance disparities across the city.

## Data

The dataset is sourced from the [NYC OpenData portal](https://opendata.cityofnewyork.us/) and contains SAT score records for NYC public high schools. It includes the following key variables:

| Column | Description |
|---|---|
| `school_name` | Name of the high school |
| `borough` | NYC borough the school is located in |
| `avg_math` | Average SAT Math score |
| `avg_reading` | Average SAT Reading score |
| `avg_writing` | Average SAT Writing score |
| `num_test_takers` | Number of students who sat the exam |

A `combined_sat` feature was engineered by summing the three individual section scores.

## Questions Answered

### 1. Which schools have the best math results?
Schools were filtered to retain only those where the average math score exceeds 80% of the maximum possible score (800 points), i.e., schools with `avg_math >= 640`. Results are ranked in descending order.

### 2. What are the top 10 schools by combined SAT score?
A `combined_sat` column was computed as the sum of the math, reading, and writing averages. The ten schools with the highest combined scores are identified and visualized.

### 3. Which borough has the largest standard deviation in SAT scores?
Borough-level descriptive statistics were computed, including the standard deviation of combined SAT scores. The borough with the greatest standard deviation exhibits the most heterogeneous distribution of school performance — indicating the widest gap between high- and low-performing schools within that administrative area.

## Tools Used

| Tool | Purpose |
|---|---|
| **Python 3** | Core programming language |
| **Pandas** | Data loading, cleaning, transformation, and aggregation |
| **Plotly** | Interactive data visualization |

## Repository Structure

```
nyc-schools-sat-analysis/
│
├── notebook.ipynb        # Main analysis notebook
├── schools.csv           # Raw dataset
└── README.md             # Project documentation
```

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/belajunker/nyc-schools-sat-analysis
   cd nyc-schools-sat-analysis
   ```

2. Install dependencies:
   ```bash
   pip install pandas plotly
   ```

3. Open and run the notebook:
   ```bash
   jupyter notebook notebook.ipynb
   ```

## Source

This project was completed as part of a guided exercise in the **[DataCamp](https://www.datacamp.com/)** Data Analyst with Python career track. The analytical questions and dataset were provided by DataCamp; the implementation and interpretation are the author's own.

