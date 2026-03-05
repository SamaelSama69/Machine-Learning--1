# 🏨 Hotel Booking Cancellation Prediction

### Machine Learning Project -- INN Hotels Group

![Python](https://img.shields.io/badge/Python-3.x-blue) ![Machine
Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange)
![EDA](https://img.shields.io/badge/Data%20Analysis-Pandas%20%7C%20NumPy-green)
![Visualization](https://img.shields.io/badge/Visualization-Matplotlib%20%7C%20Seaborn-red)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

------------------------------------------------------------------------

# 📌 Project Overview

Hotel booking cancellations are a major challenge in the hospitality
industry. Unexpected cancellations lead to:

-   Revenue loss when rooms remain unsold
-   Additional marketing costs to resell rooms
-   Operational inefficiencies
-   Reduced profit margins due to last‑minute discounts

This project builds a **machine learning solution to predict hotel
booking cancellations** for the **INN Hotels Group**, a chain of hotels
operating in Portugal.

By identifying bookings likely to cancel in advance, hotels can:

-   Improve revenue management
-   Optimize overbooking strategies
-   Reduce financial losses
-   Improve operational planning

------------------------------------------------------------------------

# 🎯 Business Objective

The goal of this project is to:

1.  Analyze historical booking data
2.  Identify factors influencing cancellations
3.  Build machine learning models to predict booking cancellations
4.  Provide actionable recommendations for hotel management

The predictive model helps hotels **anticipate cancellations and
implement proactive policies**.

------------------------------------------------------------------------

# 📊 Dataset Description

The dataset contains **36,275 hotel bookings with 19 features**
describing guest behavior, reservation details, and booking history.
fileciteturn1file0

### Key Features

  Feature                                Description
  -------------------------------------- -------------------------------------------
  Booking_ID                             Unique identifier for each booking
  no_of_adults                           Number of adults
  no_of_children                         Number of children
  no_of_weekend_nights                   Number of weekend nights booked
  no_of_week_nights                      Number of weekday nights booked
  type_of_meal_plan                      Meal plan selected
  required_car_parking_space             Parking requirement
  room_type_reserved                     Type of room reserved
  lead_time                              Days between booking and arrival
  arrival_year                           Year of arrival
  arrival_month                          Month of arrival
  arrival_date                           Day of arrival
  market_segment_type                    Booking channel
  repeated_guest                         Whether the guest stayed before
  no_of_previous_cancellations           Previous cancellations
  no_of_previous_bookings_not_canceled   Previous successful bookings
  avg_price_per_room                     Average price per room
  no_of_special_requests                 Special requests made
  booking_status                         Target variable (Canceled / Not Canceled)

------------------------------------------------------------------------

# 📂 Dataset Overview

-   **Rows:** 36,275 bookings\
-   **Columns:** 19 variables\
-   **Target Variable:** `booking_status`

The dataset contains both **categorical and numerical variables**
describing booking behavior. fileciteturn1file0

No missing values were found in the dataset.

------------------------------------------------------------------------

# 🔎 Exploratory Data Analysis

EDA was conducted to understand the distribution and relationships
between variables.

Key analysis performed:

-   Univariate analysis
-   Bivariate analysis
-   Correlation heatmap
-   Distribution plots
-   Cancellation rate analysis

### Major Findings

-   Around **33% of bookings are canceled**, representing a major
    revenue challenge. fileciteturn1file0
-   Online bookings represent the largest share of reservations.
-   Lead time is strongly associated with cancellation probability.
-   Guests with multiple special requests rarely cancel.
-   Repeated guests show significantly lower cancellation rates.

------------------------------------------------------------------------

# 📊 Customer Behavior Insights

### Booking Patterns

-   Most bookings involve **two adults**, indicating couples or small
    groups.
-   The majority of reservations have **no children**.
-   Most stays include **1--2 weekday nights**.

### Meal Plan Preferences

Meal Plan 1 (Breakfast) dominates booking selections, suggesting guests
prefer convenient breakfast options.

### Market Segment

Online channels generate the majority of bookings, followed by offline
reservations.

### Special Requests

Guests with multiple special requests are significantly **less likely to
cancel**.

------------------------------------------------------------------------

# 🧹 Data Preprocessing

The following preprocessing steps were performed before modeling:

-   Removing unnecessary identifiers (`Booking_ID`)
-   Encoding categorical variables
-   Handling skewed distributions
-   Creating new derived features
-   Preparing train/test datasets

------------------------------------------------------------------------

# 🤖 Machine Learning Models

Two models were developed and compared:

### 1️⃣ Logistic Regression

Used as a baseline classification model to estimate the probability of
cancellation.

Key steps:

-   Feature selection
-   Multicollinearity checks
-   Odds ratio interpretation
-   Threshold tuning

### 2️⃣ Decision Tree Classifier

Used to capture **non‑linear relationships between booking features and
cancellations**.

Enhancements:

-   Tree pruning
-   Hyperparameter tuning
-   Feature importance analysis

------------------------------------------------------------------------

# 📈 Model Evaluation Metrics

Models were evaluated using:

-   Accuracy
-   Precision
-   Recall
-   F1 Score
-   ROC‑AUC
-   Confusion Matrix

These metrics ensure balanced evaluation of classification performance.

------------------------------------------------------------------------

# 📊 Model Comparison

Both models were evaluated on training and testing datasets.

### Logistic Regression

Advantages:

-   Interpretable coefficients
-   Probabilistic predictions
-   Good baseline performance

### Decision Tree

Advantages:

-   Captures complex relationships
-   Handles nonlinear patterns
-   Provides feature importance insights

The final model was selected based on **overall predictive performance
and interpretability**.

------------------------------------------------------------------------

# 🔑 Key Predictors of Cancellation

The analysis revealed several features strongly associated with
cancellations:

### Lead Time

Bookings made far in advance are more likely to be canceled.

### Market Segment

Online bookings have a higher cancellation probability.

### Special Requests

Guests with more special requests are less likely to cancel.

### Previous Booking Behavior

Customers with previous cancellations are more likely to cancel again.

### Average Price

Higher room prices may increase cancellation risk.

------------------------------------------------------------------------

# 💡 Business Recommendations

Based on the model insights, several strategies can reduce cancellation
losses.

### 1️⃣ Implement Smart Overbooking

Predictive models can identify high‑risk bookings and allow controlled
overbooking.

### 2️⃣ Adjust Cancellation Policies

Stricter policies for high‑risk bookings can reduce last‑minute
cancellations.

### 3️⃣ Loyalty Incentives

Encouraging repeat guests can improve booking reliability.

### 4️⃣ Early Confirmation Discounts

Providing incentives for early payment can reduce cancellations.

### 5️⃣ Personalized Guest Engagement

Guests with special requests are less likely to cancel; improving
personalization may increase commitment.

------------------------------------------------------------------------

# 🛠 Technology Stack

  Category           Tools
  ------------------ ---------------------
  Programming        Python
  Data Analysis      Pandas, NumPy
  Visualization      Matplotlib, Seaborn
  Machine Learning   Scikit‑Learn
  Environment        Jupyter Notebook

------------------------------------------------------------------------

# 📁 Project Structure

    hotel-booking-cancellation-prediction
    │
    ├── data
    │   └── hotel_bookings.csv
    │
    ├── notebooks
    │   └── INNHotels_project.ipynb
    │
    ├── report
    │   └── machine_learning_project_report.pdf
    │
    ├── models
    │   └── trained_models
    │
    └── README.md

------------------------------------------------------------------------

# ⭐ Future Improvements

Several enhancements can further improve the system:

-   Random Forest model
-   Gradient Boosting models
-   XGBoost implementation
-   Hyperparameter tuning
-   Deployment using Streamlit
-   Real‑time cancellation prediction dashboard

------------------------------------------------------------------------

# 👨‍💻 Author

**Sham Solanki**\
Master's in Data Science -- Deakin University

------------------------------------------------------------------------

# 📜 License

This project is licensed under the **MIT License**.
