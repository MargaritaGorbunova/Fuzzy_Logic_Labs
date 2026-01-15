# Lab 3: Defuzzification of Fuzzy Sets

## Project Overview
Defuzzification of a fuzzy set with a trapezoidal membership function using various methods, with a comparative analysis of their features and application areas.

## Objectives
* Perform defuzzification using all maxima methods at truncation level **k = 0.5**
* Perform defuzzification using center of gravity method for full membership functions at **k = 0.5**
* Perform defuzzification using center of gravity method for alpha-cut at **k = 0.4**
* Analyze differences between defuzzification methods

## Input Data
Fuzzy set **"Medium"** with trapezoidal membership function:
* **Support:** (28.4118; 62.0736)
* **Core:** [35; 50]
* **Height:** 1
* **α-cut at α=0.4:** [31.047; 57.244]

## Results
### Defuzzification Methods Comparison

| Method | Acronym | Value | Description |
| :--- | :--- | :--- | :--- |
| First of Maxima | FOM | 35.0 | Smallest value from core in truncated region |
| Last of Maxima | LOM | 50.0 | Largest value from core in truncated region |
| Mean of Maxima | MOM | 42.5 | Average of FOM and LOM |
| Center of Gravity (Full) | COG | 43.6 | Center of mass of entire membership function |
| Center of Alpha-cut | COA | 44.15 | Midpoint of α-cut interval |

### Method Details
**Maxima Methods (k = 0.5):**
* Truncation interval: [31.7059; 56.0368]
* Core within interval: [35; 50]
* FOM takes left boundary (35)
* LOM takes right boundary (50)
* MOM calculates average (42.5)

**Center of Gravity Methods:**
* **COG:** Integrates over entire function shape
* **COA:** Uses simple midpoint of α-cut boundaries

## Conclusions
* Maxima methods are computationally simple but use limited information (only core boundaries)
* Center of Gravity (COG) provides most accurate result by considering entire function shape
* Center of Alpha-cut (COA) offers simplest calculation but ignores shape details
* Results range from 35.0 to 44.15 due to function asymmetry (right slope longer than left)
* Method selection depends on application requirements: speed vs. accuracy

## Files
* `report_lab3.pdf` – Complete laboratory report with detailed calculations
* `calculations_lab3.xlsx` – Numerical computations and visualizations
