
This project analyzes customer data for an Amazon clothing sales platform to determine whether to focus efforts on the mobile app or website. Using linear regression, we predict the "Yearly Amount Spent" based on numerical features like average session length, time on app, time on website, and length of membership.
Dataset

Source: output.csv
Columns:
Email: Customer email (dropped for analysis)
Address: Customer address (dropped for analysis)
Avatar: Customer avatar (dropped for analysis)
Avg. Session Length: Average time spent in styling sessions (float)
Time on App: Time spent on the mobile app (float)
Time on Website: Time spent on the website (float)
Length of Membership: Duration of customer membership (float)
Yearly Amount Spent: Target variable, amount spent annually (float)


Rows: 500
Null Values: None

Dependencies

Python 3.x
Libraries:
pandas: Data manipulation and DataFrame operations
numpy: Numerical computations
matplotlib.pyplot: Plotting and visualization
seaborn: Advanced statistical visualizations
sklearn: Machine learning tools (train_test_split, LinearRegression)



Steps

Data Loading and Cleaning

Load output.csv into a pandas DataFrame (customers)
Drop non-numerical columns: Email, Address, Avatar
Resulting features: Avg. Session Length, Time on App, Time on Website, Length of Membership
Target: Yearly Amount Spent


Exploratory Data Analysis

Use customers.describe() and customers.info() to understand data distribution and types
Visualizations:
Jointplot: Time on Website vs. Yearly Amount Spent
Jointplot: Time on App vs. Yearly Amount Spent
Hex bin jointplot: Time on App vs. Length of Membership
Pairplot: All numerical features
Linear model plot: Yearly Amount Spent vs. Length of Membership




Data Preparation

Define features (X): Avg. Session Length, Time on App, Time on Website, Length of Membership
Define target (y): Yearly Amount Spent
Split data into training (70%) and testing (30%) sets using train_test_split (random_state=101)


Model Training

Create a LinearRegression model instance (lm)
Fit the model on training data (X_train, y_train)
Extract coefficients to understand feature importance


Prediction and Evaluation

Predict on test set (X_test) using lm.predict()
Visualize real vs. predicted values with a scatterplot
Coefficients indicate the impact of each feature on Yearly Amount Spent



Key Findings

Coefficients from the model:
Avg. Session Length: ~26.33
Time on App: ~38.53
Time on Website: ~0.16
Length of Membership: ~61.35


Insight: Length of Membership and Time on App have the strongest positive influence on spending, while Time on Website has minimal impact. This suggests focusing efforts on the mobile app experience.

Usage

Install dependencies: pip install pandas numpy matplotlib seaborn scikit-learn
Ensure output.csv is in the working directory
Run the Python script to:
Load and clean data
Visualize relationships
Train the linear regression model
Evaluate predictions



Notes

The scatterplot of real vs. predicted values helps assess model fit
Adjust test_size or random_state in train_test_split for different splits
Ensure matplotlib.pyplot is imported to avoid NameError in plotting

Recommendation
Based on the model, prioritize the mobile app experience, as Time on App has a significantly higher coefficient (38.53) compared to Time on Website (0.16), indicating a stronger relationship with customer spending.
