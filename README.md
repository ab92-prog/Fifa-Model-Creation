# Goalkeeper Performance Prediction Model

This is my first-ever machine learning model, created as a challenge given by my mentor, Mr. Unrvinder Singh. The task was to predict the performance of goalkeepers using various variables of my choice. The dataset provided contains 18,000 entries and 89 columns.

## Dataset Analysis

After exploring the dataset, I performed some data visualizations using Seaborn to better understand the data:

- **Age Range of Players:**
  - 15-20: 4758 players
  - 20-25: 6736 players
  - 25-30: 4846 players
  - 30-35: 1709 players
  - 35-40: 162 players
  - 40-15: 4 players

- **Potential of Players:**
  - 50-60: 200 players
  - 60-70: 5000 players
  - 70-80: 10000 players
  - 80-90: 2000 players
  - 90-100: 100 players

- **Preferred Foot:**
  - Right Foot: 14,000 players
  - Left Foot: 4,000 players

Based on these visualizations, I decided to drop 42 unnecessary columns using my knowledge of football and correlation analysis.

## Model Creation

I started by creating a linear regression model, which resulted in an R-squared value of only 22%. Unsatisfied with this result, I built another model using the `stats models` library, which significantly improved the predictions.

## OLS Regression Results

Here are the results of the Ordinary Least Squares (OLS) Regression:

```
Dep. Variable: Overall
R-squared: 0.177
Adj. R-squared: 0.177
F-statistic: 654.5
Prob (F-statistic): 0.00
Log-Likelihood: -59246.
No. Observations: 18207
AIC: 1.185e+05
Df Residuals: 18200
BIC: 1.186e+05
Df Model: 6
Covariance Type: nonrobust

|               | coef     | std err | t        | P>|t|     [0.025   0.975]  |
|---------------|----------|---------|----------|---------|---------------------|
| const         | 52.7230  | 0.230   | 229.246  | 0.000   | 52.272   53.174   |
| GKDiving      | 0.0087   | 0.014   | 0.622    | 0.534   | -0.019   0.036    |
| GKHandling    | 0.0182   | 0.014   | 1.297    | 0.195   | -0.009   0.046    |
| GKKicking     | -0.0440  | 0.013   | -3.381   | 0.001   | -0.069   -0.018   |
| GKPositioning | 0.1017   | 0.014   | 7.380    | 0.000   | 0.075    0.129    |
| GKReflexes    | 0.0395   | 0.014   | 2.859    | 0.004   | 0.012    0.067    |
| Penalties     | 0.2361   | 0.004   | 62.170   | 0.000   | 0.229    0.244    |
```

## Conclusion

The model's performance is moderate, with an R-squared value of 0.177. Further improvements can be made by exploring more features or trying different machine learning algorithms.

## How to Run

To run the code and recreate the model:

1. Clone this repository.
2. Ensure you have the required dependencies installed. (List dependencies here)
3. Run the Jupyter Notebook or Python script (provide filenames) to train the model.
4. The trained model will provide predictions based on the input data.

## Contributions

Contributions to this project are welcome!

## License

This project is licensed under the [MIT License](LICENSE). 
