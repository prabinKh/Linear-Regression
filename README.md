🌟 Amazon Clothing Sales: Unveiling Insights with Linear Regression 🌟
🚀 Project Overview
Welcome to an exciting journey into the world of Amazon clothing sales! This project dives deep into customer data to help decide: should we supercharge our mobile app or revamp our website? Using the power of linear regression, we predict the "Yearly Amount Spent" based on key factors like session length, app usage, website time, and membership duration. Get ready to uncover game-changing insights!
🎨 The Dataset: A Treasure Trove

Source: output.csv
Golden Columns:
Email: Customer emails (dropped for analysis)
Address: Customer addresses (dropped for analysis)
Avatar: Unique avatars (dropped for analysis)
Avg. Session Length: Time spent with stylists (float)
Time on App: Minutes on the mobile app (float)
Time on Website: Minutes browsing the site (float)
Length of Membership: Loyalty in years (float)
Yearly Amount Spent: The star of the show—annual spending! (float)


Scale: 500 dazzling rows
Quality: Zero missing values—pure, clean data!

🛠️ Tools of the Trade

Python 3.x: The engine of our adventure
Powerhouse Libraries:
pandas: Crafting data with finesse
numpy: Crunching numbers like a pro
matplotlib.pyplot: Stunning visualizations
seaborn: Elegant, insightful plots
sklearn: Machine learning magic



🌈 The Journey: Step by Step

Data Prep: Polishing the Gem

Load output.csv into a sparkling customers DataFrame
Trim the extras: Drop Email, Address, and Avatar
Focus on the stars: Avg. Session Length, Time on App, Time on Website, Length of Membership
Target the prize: Yearly Amount Spent


Exploration: A Visual Feast

Peek at stats with customers.describe() and customers.info()
Dazzling Visuals:
Jointplot: Time on Website vs. Yearly Amount Spent—a subtle dance
Jointplot: Time on App vs. Yearly Amount Spent—a fiery connection
Hex Bin Plot: Time on App vs. Length of Membership—a honeycomb of insight
Pairplot: A gallery of all numerical features
Linear Model Plot: Yearly Amount Spent vs. Length of Membership—a trend to behold




Gear Up: Splitting the Data

Features (X): Avg. Session Length, Time on App, Time on Website, Length of Membership
Target (y): Yearly Amount Spent
Split with flair: 70% training, 30% testing via train_test_split (random_state=101)


Training: Unleashing the Model

Summon a LinearRegression model, named lm
Train it on X_train and y_train—watch it learn!
Reveal the coefficients: The secret sauce of feature impact


Prediction: The Grand Reveal

Predict with lm.predict() on X_test
Visualize the magic: Scatterplot of real vs. predicted values
Coefficients light the way to strategic brilliance



💡 Dazzling Insights

Model Coefficients:
Avg. Session Length: ~26.33—solid influence
Time on App: ~38.53—a shining star
Time on Website: ~0.16—a faint whisper
Length of Membership: ~61.35—the crown jewel


Big Reveal: Length of Membership and Time on App drive spending to the skies, while Time on Website barely nudges the needle. The mobile app is your golden ticket!

🎉 How to Dive In

Install the magic: pip install pandas numpy matplotlib seaborn scikit-learn
Place output.csv in your working directory
Run the script to:
Clean and prep the data
Feast on vibrant visualizations
Train a stellar linear regression model
Witness prediction power


