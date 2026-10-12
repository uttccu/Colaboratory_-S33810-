# Google Colab: Apartment price regression

Completed linear regression tutorial with all five independent exercises.

## Run
Open `colab_regression.ipynb` in Google Colab and choose **Runtime → Run all**.
Upload `apartments.csv` to the runtime if desired. The notebook includes the exact
six supplied rows as a fallback, so it also runs without uploading the CSV.
For local execution: `pip install -r requirements.txt`, then open the notebook
in Jupyter (install Jupyter separately if needed).

## Results
Linear equation (price in thousands of PLN):
`price = 5.445000 * area_m2 + 120.791667`.

Predictions:
| area_m2 | predicted_price_thousands_pln | predicted_price_pln |
| --- | --- | --- |
| 40 | 338.5917 | 338591.6667 |
| 60 | 447.4917 | 447491.6667 |
| 80 | 556.3917 | 556391.6667 |

Model comparison:
| model | training_MAE | training_MSE | training_RMSE | training_R2 | LOO_MAE | LOO_MSE | LOO_RMSE |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Linear | 3.4250 | 13.4514 | 3.6676 | 0.9995 | 5.3359 | 34.5478 | 5.8777 |
| Quadratic | 2.7691 | 10.9384 | 3.3073 | 0.9996 | 6.5894 | 63.4390 | 7.9649 |

Training MAE/RMSE and LOO MAE/RMSE are in thousands of PLN.
MSE is in squared thousands of PLN. R2 is dimensionless.
LOO means leave-one-out cross-validation: train on five rows and predict the sixth.
The linear model has lower LOO MAE on this small sample.
Six illustrative rows are insufficient to establish real housing-market accuracy.

## Completed exercises
- Add `price_per_m2`, with conversion to PLN/m².
- Plot area against price per m².
- Calculate MAE, MSE, RMSE and R2.
- Fit an area-plus-area² model and compare training and cross-validation errors.
- Save `regression.png`, `price_per_m2.png` and `model_comparison.png`.

The notebook includes executed outputs. CSV files contain predictions, derived
unit prices and the model comparison.

## Submission
Create a repository named `Colaboratory_<student-number>` in `PRO-D-PJATK`.
Upload the contents of this project folder and submit the repository link in Teams.

## Source
Data and assignment: https://github.com/PRO-D-PJATK/tutorials/tree/main/google-colab-linear-regression
