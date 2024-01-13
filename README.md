# Coffee Degradation Prediction

## Overview

This project focuses on predicting coffee degradation using taste notes. The goal is to provide a tool for coffee quality assessment based on the input of taste characteristics. The project encompasses various stages, including data preprocessing, feature reduction, machine learning model implementation, and evaluation.

## Project Structure

- **Data Preparation:**
  - The project starts with data loading from an Excel file (`2018_2019_2020_DataSheet.xlsx`).
  - Relevant columns, such as 'Taste Notes,' 'Score,' and 'PSS,' are selected.
  - Data cleaning involves handling missing values, converting data types, and calculating the 'Delta' column.

- **Feature Reduction:**
  - A feature reduction strategy is implemented to categorize taste notes into a concise set of "Taste Categories."
  - Similarity calculations and a predefined set of notes aid in categorization.

- **Data Visualization:**
  - The shaped data is visualized, focusing on the distribution of change in coffee quality.
  - Adjustments are made to enhance clarity, and taste notes are preprocessed for Natural Language Processing (NLP).

- **Machine Learning Models:**
  - A linear regression model is utilized as part of the feature reduction method.
  - Further, a Random Forest Regression model is implemented, employing optimal taste notes determined earlier.
  - Hyperparameter tuning is performed using GridSearch for the Random Forest model.

- **Results Analysis:**
  - Various metrics, such as Mean Squared Error (MSE), R-squared, and a paired t-test, are employed to evaluate model performance.
  - The project concludes with a comprehensive analysis, comparing the Random Forest model against a mean delta approach.

## Usage: Predict Coffee Degradation

To predict coffee degradation based on new taste notes, use one of the two `predict_coffee_degradation` functions.

```python
# Example Usage:
new_taste_notes_input = "citrus, chocolate, nutty"
predict_coffee_degradation(new_taste_notes_input)
```

This function preprocesses the input taste notes, vectorizes them using the TF-IDF vectorizer, and predicts the delta using the trained Random Forest model. The result is the predicted delta for the new taste notes.

Feel free to experiment with different taste note combinations to assess coffee quality predictions.
