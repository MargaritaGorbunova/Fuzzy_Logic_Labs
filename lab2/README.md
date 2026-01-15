# Lab 2: Fuzzy Set Operations and Properties

## Project Overview
Experimental investigation of fuzzy set properties and operations based on membership functions derived from expert evaluations for mobile robot control.

## Objectives
- Verify normality and normalize membership functions if needed
- Determine fuzzy set properties (support, crisp/fuzzy regions, α-cut)
- Apply operations to single fuzzy sets
- Perform operations between two fuzzy sets

## Results

### Set Properties (α = 0.4)

| Term | Function | Support | Fuzzy Region | α-cut |
|------|----------|---------|--------------|-------|
| Very Close | Z-function | [0; 21.709) | (9.523; 21.709) | [0; 15.579] |
| Close | Π-function | (5.829; 37.08) | (5.829; 20) ∪ (29.871; 37.08) | [11.497; 34.196] |
| Medium | Π-function | (28.412; 62.074) | (28.412; 35) ∪ (50; 62.074) | [31.047; 57.244] |
| Far | S-function | [46.703; +∞) | (46.703; 60) | [52.022; +∞) |

### Operations on Single Set ("Close")
- **Complement**: Inverted membership values
- **Multiplication (k=0.7)**: Scaled membership
- **Expansion (to 0.3)**: Widened fuzzy region
- **Truncation (at 0.5)**: Clipped membership
- **Concentration (β=1.6)**: Sharper transition
- **Dilation (β=0.6)**: Smoother transition

### Operations Between "Close" and "Medium"
- **Equivalence (A = B)**: Minimum of memberships
- **Inclusion (A ⊆ B, B ⊆ A)**: Subset relationships
- **Union (A ∪ B)**: Maximum of memberships
- **Intersection (A ∩ B)**: Minimum of memberships
- **Algebraic Multiplication (A·B)**: Product of memberships
- **Algebraic Addition (A+B)**: Sum minus product

## Conclusions
- All sets confirmed as normal (max μ = 1)
- Operation results require piecewise mathematical descriptions
- Fuzzy set apparatus provides flexible modeling of expert knowledge
- Ready for integration into fuzzy inference system

## Files
- `report_lab2.pdf` – complete laboratory report
- `calculations_lab2.xlsx` – all computations and visualizations
