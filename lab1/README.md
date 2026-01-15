# Lab 1: Fuzzy Membership Functions for "Distance to Obstacle"

## Project Overview
Experimental determination of membership functions for the linguistic variable **"Distance to Obstacle"** using group expert evaluations. The models are intended for integration into a fuzzy control system for a mobile robot.

## Objectives
- Survey 8 experts to define boundaries for linguistic terms.
- Preprocess and structure expert data.
- Identify standard membership function shapes.
- Perform parametric identification using the least squares method.
- Evaluate model accuracy.

## Linguistic Terms
- Very Close (Очень_близко)
- Close (Близко)
- Medium (Средне)
- Far (Далеко)

Universal set: 0–200 cm.

## Methodology
1. **Structural Identification:** Assign standard function shapes based on data trends.
2. **Parametric Identification:** Optimize function parameters using Excel Solver (least squares).
3. **Accuracy Evaluation:** Calculate MSE, MAE, and MaxAE.

## Results

### Selected Functions & Parameters
| Term          | Function Type | Fuzzy Region (cm)        |
|---------------|---------------|--------------------------|
| Very Close    | Z-function    | 12.186                   |
| Close         | Π-function    | Left: 14.171, Right: 7.209 |
| Medium        | Π-function    | Left: 6.588, Right: 12.074 |
| Far           | S-function    | 13.297                   |

### Model Accuracy
| Term          | MSE    | MAE    | MaxAE  |
|---------------|--------|--------|--------|
| Very Close    | 0.004  | 0.056  | 0.105  |
| Close         | 0.023  | 0.119  | 0.228  |
| Medium        | 0.007  | 0.067  | 0.134  |
| Far           | 0.015  | 0.106  | 0.173  |

## Conclusions
- Standard membership function shapes were successfully matched to expert data.
- Most terms are well-described by linear transitions; *Very Close* required a quadratic correction (k=0.0028).
- Highest accuracy achieved for *Medium* (MSE=0.022), lowest for *Close* (MSE=0.093).
- The obtained models are ready for use in a fuzzy inference system for mobile robot control.

## Files
- `report_lab1.pdf` – full laboratory report (in Russian)
- `calculations_lab1.xlsx` - all computations and visualizations
