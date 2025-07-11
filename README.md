# Salary Prediction Model Using Linear Regression

## Overview
This project implements a linear regression model to predict an employee's salary based on their years of experience. The model is built using Python and leverages libraries such as pandas, numpy, scikit-learn, and matplotlib for data handling, model building, evaluation, and visualization.

## Dataset
The dataset used is `Salary_data.csv`, which contains two columns:
- **YearsExperience**: The number of years of professional experience (feature).
- **Salary**: The corresponding annual salary in dollars (target).

The dataset is loaded with encoding handling to manage potential issues (e.g., UTF-8, latin1). If the file is unavailable, ensure the correct file path is specified.

## Prerequisites
To run this project, ensure you have the following Python libraries installed:
```bash
pip install pandas numpy scikit-learn matplotlib
```

## Project Structure
The main code is provided in a Jupyter Notebook: `Linear Regression - Salary Prediction Model.ipynb`. The notebook is divided into the following steps:

1. **Set Up the Environment**: Import necessary libraries (pandas, numpy, scikit-learn, matplotlib).
2. **Load the Dataset**: Read the `Salary_data.csv` file with encoding handling.
3. **Prepare the Data**: Extract features (YearsExperience) and target (Salary) for the model.
4. **Create and Train the Model**: Train a linear regression model to learn the relationship between years of experience and salary.
5. **Evaluate the Model**: Compute Mean Squared Error (MSE) and R² score to assess model performance.
6. **Make Predictions**: Allow user input for years of experience to predict salary.
7. **Visualize Results**: Plot a scatter of actual data points with the regression line.
8. **Interpret and Improve**: Analyze the model’s performance and suggest improvements (e.g., handling outliers, trying polynomial regression).

## How to Run
1. **Clone or Download**: Download the Jupyter Notebook and the dataset (`Salary_data.csv`).
2. **Set Up Environment**: Ensure all required libraries are installed.
3. **Update File Path**: In Step 2 of the notebook, update the `file_path` variable to the location of `Salary_data.csv` on your system.
4. **Run the Notebook**: Execute the notebook cells sequentially in a Jupyter environment (e.g., Jupyter Notebook, Google Colab).
5. **Input Experience**: When prompted, enter the years of experience to get a predicted salary.
6. **View Results**: Check the console output for model metrics (MSE, R²) and the plot showing the regression line.

## Model Details
- **Algorithm**: Linear Regression (y = mx + b, where m is the slope and b is the intercept).
- **Features**: Single feature (YearsExperience).
- **Target**: Salary.
- **Evaluation Metrics**:
  - **Mean Squared Error (MSE)**: Measures the average squared difference between actual and predicted salaries.
  - **R² Score**: Indicates the proportion of variance in salary explained by years of experience (closer to 1 is better).
- **Visualization**: A scatter plot of actual data points with the fitted regression line.

## Example Output
For the sample dataset:
- Model equation: `Salary = 9449.96 * YearsExperience + 25792.20`
- MSE: ~31,270,951.72 (depends on the dataset scale).
- R² Score: ~0.96 (indicating a strong linear fit).
- Prediction for 5.6 years: ~$78,711.99.

## Improvements
- **Outlier Handling**: Remove extreme values using quantile-based filtering.
- **Non-linear Models**: If the data shows non-linear trends, consider polynomial regression.
- **Cross-Validation**: Use `cross_val_score` to assess model robustness.
- **Feature Engineering**: Add more features (e.g., job role, education) for better predictions if available.

## Notes
- Ensure the dataset is clean (no missing values) before running the model.
- The model assumes a linear relationship between experience and salary. If the relationship is non-linear, consider advanced models.
- The code includes error handling for invalid user input (e.g., non-numeric values).

## License
This project is for educational purposes and uses standard open-source Python libraries.