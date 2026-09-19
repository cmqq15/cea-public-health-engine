
# Automated Cost-Effectiveness Analysis Engine

This project demonstrates a reproducible cost-effectiveness analysis (CEA) workflow for public-health interventions using simulated data.

## Contents

- `Project4_revised.ipynb`: revised notebook with validation, reproducible simulation, transparent assumptions, ranking, and limitations.
- `requirements.txt`: Python dependencies.

## What was fixed

1. **Reproducibility:** Added a fixed random seed using NumPy's modern random-number generator.
2. **Unit consistency:** Costs are calculated for a defined cohort and divided by DALYs averted for that same cohort.
3. **Input validation:** Added checks for missing values, invalid proportions, negative costs, non-positive DALYs, and undefined ratios.
4. **Threshold framing:** Replaced the unqualified “3 × GDP per capita” rule with a configurable, explicitly illustrative willingness-to-pay threshold.
5. **Methodological transparency:** Clarified that simulated DALYs are demonstration inputs, not a formal DALY estimation model.
6. **Interpretation:** Added limitations and next steps covering perspective, comparator, time horizon, discounting, uncertainty, affordability, and equity.
7. **Presentation:** Added readable ranking output and explanatory Markdown sections.

## Installation

Create and activate a virtual environment, then install the dependencies:

```bash
python -m venv .venv
source .venv/bin/activate       # macOS/Linux
# .venv\\Scripts\\activate    # Windows PowerShell
pip install -r requirements.txt
```

## Running the notebook

```bash
jupyter notebook Project4_revised.ipynb
```

Run all cells from top to bottom. The notebook uses simulated inputs and should not be used to make real resource-allocation decisions without replacing them with validated data.

## Analytical caveat

The notebook ranks interventions by average cost per DALY averted. A full economic evaluation should generally specify a comparator and calculate incremental costs and effects, with an explicit perspective, time horizon, discount rate, currency year, uncertainty analysis, and decision rule.
