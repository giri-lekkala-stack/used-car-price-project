# What Drives the Price of a Used Car?

## Business question

This project analyzes used-car listings to help a dealership make better inventory acquisition and pricing decisions. The central question is: which vehicle attributes are most associated with listing price?

## Key findings

- Age and odometer reading are foundational pricing inputs: newer, lower-mileage vehicles tend to command higher prices.
- Pricing differs substantially by manufacturer, body type, drive train, fuel type, and transmission. Inventory should be compared within its segment, not to the overall market average.
- Title status and condition are important risk signals. Clean-title vehicles with complete condition details should receive priority during acquisition.
- The selected model should be used as a pricing guardrail, then adjusted for inspection findings, reconditioning costs, local demand, and inventory velocity.

## Recommendation for dealers

Require year, mileage, title status, condition, manufacturer, type, drive, fuel, and transmission before making an offer. Use a model estimate to flag listings that appear overpriced or underpriced, but keep a human review step for vehicle-specific condition and local market factors.

## Repository contents

| Path | Purpose |
| `notebooks/used_car_price_analysis.ipynb` | Full CRISP-DM analysis, charts, regression models, cross-validation, grid search, and dealer recommendations. |
| `data/vehicles.csv` | Source dataset; download separately and do not commit it to GitHub. |
| `requirements.txt` | Python packages required to run the notebook. |

## How to run

1. Download and extract the assignment starter data so that `data/vehicles.csv` exists.
2. Create an environment and install dependencies: `pip install -r requirements.txt`
3. Open and run `notebooks/used_car_price_analysis.ipynb` from top to bottom.

The notebook uses a reproducible 50,000-row modeling sample and a fixed random seed. It compares Ridge regression with Random Forest regression using 5-fold cross-validation and GridSearchCV. MAE is the primary performance measure because it represents the average dollar error in a price estimate.

## Data source

Used car dataset supplied with the course practical application, derived from Craigslist vehicle listings.
