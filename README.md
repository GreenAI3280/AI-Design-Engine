'''
README for AI Design Engine

Overview
--------
This Python 3.12 script implements a simplified AI-driven design engine for early-stage building massing optimization. It combines:

- A surrogate thermal model trained via XGBoost
- A genetic algorithm implemented with PyTorch for design optimization
- A thermal simulation stub using OpenStudio-SDK Python bindings

The engine ingests basic climate data and site parameters, evolving massing options to minimize energy-use intensity (EUI). Outputs are top candidate designs with predicted energy performance.

Requirements
------------
- Python 3.12
- PyTorch
- XGBoost
- OpenStudio-SDK (Python bindings)
- pandas
- numpy

Installation
------------

```bash
pip install torch xgboost openstudio-sdk pandas numpy
```

Usage
-----

```bash
python ai_design_engine.py --data data/building_data.csv --climate data/climate.csv --runs 50
```

Arguments:
- `--data`: CSV file with training data for surrogate model (features + EUI target)
- `--climate`: CSV file with site-specific climate parameters
- `--runs`: Number of GA generations (default=100)

Outputs
-------
- `xgb_model.json`: trained surrogate model
- `best_designs.csv`: top design parameters and predicted EUI

'''  
