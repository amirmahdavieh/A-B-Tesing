# Cookie Cats A/B Testing Analysis

This repository contains a Jupyter notebook that analyzes the impact of moving the first gate in the Cookie Cats game from level 30 to level 40 on player retention and the average number of game sessions. The analysis is performed using an A/B test approach, with data provided in the `cookie_cats.txt` file.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Steps of Analysis](#steps-of-analysis)
- [Dependencies](#dependencies)
- [Usage](#usage)


## Introduction

Cookie Cats is a popular mobile puzzle game developed by Tactile Entertainment. In this notebook, we analyze an A/B test where the first gate in the game was moved from level 30 to level 40. The primary goals are to determine if:
1. The average number of game sessions has increased by 5 sessions.
2. Player retention has increased by 2% after 1 day.
3. Player retention has increased by 5% after 7 days.

## Dataset

The dataset `cookie_cats.txt` includes the following columns:
- `userid`: Unique identifier for each player.
- `version`: Indicates whether the player is in the control group (`gate_30`) or the treatment group (`gate_40`).
- `sum_gamerounds`: The total number of game rounds played by the player during the first 14 days after installation.
- `retention_1`: Whether the player returned and played the game 1 day after installation.
- `retention_7`: Whether the player returned and played the game 7 days after installation.

## Steps of Analysis

### 1. Define the Problem

We analyze the impact of moving the gate from level 30 to level 40 on player retention and game sessions.

### 2. General Analysis

- Import and inspect the dataset.
- Identify and remove duplicate user IDs.
- Detect and remove outliers using the Interquartile Range (IQR) method.

### 3. Question 1: Has the average number of game sessions increased by 5 sessions?

- Define the control group (`gate_30`) and treatment group (`gate_40`).
- Calculate and compare the average number of game sessions between the two groups using a two-sample t-test.

### 4. Question 2: Has player retention increased by 2% after 1 day?

- Define the control group (`gate_30`) and treatment group (`gate_40`).
- Calculate the required sample size for detecting a 2% increase in retention using a z-test for proportions.
- Conduct the z-test to compare retention rates after 1 day between the two groups.

### 5. Question 3: Has player retention increased by 5% after 7 days?

- Define the control group (`gate_30`) and treatment group (`gate_40`).
- Calculate the required sample size for detecting a 5% increase in retention using a z-test for proportions.
- Conduct a chi-square test to compare retention rates after 7 days between the two groups.

## Dependencies

The following Python libraries are required to run the notebook:
- pandas
- seaborn
- matplotlib
- scipy
- statsmodels

You can install these dependencies using `pip`:

```bash
pip install pandas seaborn matplotlib scipy statsmodels
```

## Usage

1. Clone the repository:

```bash
git clone https://github.com/amirmahdavieh/cookie-cats-ab-test.git
cd cookie-cats-ab-test
```

2. Open the Jupyter notebook:

```bash
jupyter notebook cookie_cats_ab_test.ipynb
```

3. Follow the steps in the notebook to analyze the data.

