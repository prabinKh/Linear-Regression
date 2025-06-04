
# 🌟 Amazon Clothing Sales: Mobile App vs. Website Focus Analysis 🌟

Welcome to the Amazon Clothing Sales Linear Regression Analysis! This project dives into customer data to help decide whether to boost the mobile app or website experience for an online clothing store. Using powerful linear regression, we predict yearly spending and uncover key insights to supercharge business strategy! 🚀

## 🎯 Project Mission
Amazon's clothing platform lets customers meet personal stylists in-store, then order online via mobile app or website. Our goal? Predict yearly spending and determine where to focus efforts—mobile app or website—using data-driven insights from linear regression! 📊

## 📊 Dataset Snapshot
- **File**: `output.csv`
- **Features**:
  - **Avg. Session Length**: Time with stylists (float)
  - **Time on App**: Mobile app usage time (float)
  - **Time on Website**: Website browsing time (float)
  - **Length of Membership**: Membership duration (float)
- **Target**: Yearly Amount Spent (float)
- **Dropped**: Email, Address, Avatar (non-numerical)
- **Rows**: 500 | **Null Values**: Zero! ✅

## 🛠️ Tools & Tech
- **Python 3.x** 🐍
- **Libraries**:
  - `pandas`: Data wrangling magic
  - `numpy`: Number-crunching power
  - `matplotlib.pyplot`: Stunning visualizations
  - `seaborn`: Sleek, stylish plots
  - `scikit-learn`: Machine learning mastery
- **Install**: `pip install pandas numpy matplotlib seaborn scikit-learn`

## 🚀 How It Works

### 1. Load & Clean
- Import `output.csv` into a pandas DataFrame
- Drop Email, Address, and Avatar for a lean dataset

### 2. Explore the Data
- Peek at stats with `describe()` and `info()`
- Visualize with flair:
  - 📈 **Jointplots**: Time on Website vs. Spending, Time on App vs. Spending
  - � **Hexbin Plot**: Time on App vs. Length of Membership
  - 🌐 **Pairplot**: All features at a glance
  - 📉 **Linear Model Plot**: Spending vs. Membership Length

### 3. Prep for Action
- **X**: Features (Avg. Session Length, Time on App, Time on Website, Length of Membership)
- **y**: Target (Yearly Amount Spent)
- **Split**: 70% training, 30% testing (random_state=101)

### 4. Train the Model
- Fire up a `LinearRegression` model
- Fit it to training data and reveal coefficients

### 5. Predict & Evaluate
- Predict spending on test data
- Scatterplot: Real vs. predicted values for a visual win!

## 🔥 Key Insights
- **Model Coefficients**:
  - Avg. Session Length: ~26.33
  - Time on App: ~38.53
  - Time on Website: ~0.16
  - Length of Membership: ~61.35
- **Big Reveal**:
  - 🏆 Length of Membership rules spending!
  - 📱 Time on App packs a punch (38.53) vs. Time on Website (0.16)
- **Verdict**: Focus on the mobile app for maximum impact! 🚀

## 🏃 Quick Start
1. Clone this repo:  
   `git clone https://github.com/your-username/amazon-clothing-sales-analysis.git`
2. Install dependencies:  
   `pip install pandas numpy matplotlib seaborn scikit-learn`
3. Place `output.csv` in the project folder
4. Run the script and watch the magic unfold!
   - Explore data
   - Train the model
   - Visualize predictions

