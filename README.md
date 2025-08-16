Sparkify User Churn Prediction Project 🎵

# Overview
Sparkify is a music streaming service, similar to Spotify or Apple Music. This project analyzes user behavior data to predict customer churn using Apache Spark and Machine Learning techniques. The goal is to identify users who are likely to cancel their subscription before they actually do, enabling the business to take proactive retention measures.

# 📋 Project Description
This project uses a dataset containing user interaction logs from the Sparkify music streaming platform. 
The analysis includes:
  1. Data Cleaning & Preprocessing: Handling missing values and filtering relevant user sessions
  2. Exploratory Data Analysis: Understanding user behavior patterns and identifying churn indicators
  3. Feature Engineering: Creating meaningful features from raw interaction data
  4. Machine Learning: Training and evaluating multiple classification models to predict user churn
  5. Model Comparison: Evaluating different algorithms including Gradient Boosting, Logistic Regression, Decision Trees, and Random Forest
     
# 🗃️ Dataset
The project uses the Sparkify event dataset which contains: 
  1. Size: 128MB subset (full dataset is 12GB)
  2. Format: JSON format with user interaction logs
  3. Records: ~286,500 interaction events

# 🎯 Churn Definition
The analysis works on a definition of "Churn" segmentation. The user is considered “churned” if they visit the “Cancellation Confirmed” page, indicating they have cancelled their subscription. The dataset shows a churn rate of approximately 23%.

# 🔧 Technologies Used
Big Data & Spark
    • Apache Spark: Distributed data processing
    • PySpark: Python API for Spark
    • Spark MLlib: Machine learning library
Machine Learning
    • Gradient Boosting Trees (GBT)
    • Logistic Regression
    • Decision Trees
    • Random Forest
    • Cross-validation and Grid Search
Data Analysis & Visualization
    • Pandas: Data manipulation
    • NumPy: Numerical computing
    • Matplotlib: Data visualization
    • Seaborn: Statistical visualization

# 🚀 Getting Started

Prerequisites
## Required Software
- Python 3.7+
- Apache Spark 3.x
Installation
    1. Clone the repository
git clone <repository-url>
cd sparkify-churn-prediction
    2. Set up Java environment
export JAVA_HOME=/path/to/java
export PATH=$JAVA_HOME/bin:$PATH
    3. Install Python dependencies
pip install pyspark pandas numpy matplotlib seaborn
Running the Project
    1. Start the notebook
jupyter notebook sparkify_5.ipynb
    2. Or run specific sections
        ◦ Data loading and cleaning
        ◦ Exploratory data analysis
        ◦ Feature engineering
        ◦ Model training and evaluation

# 🎯 Model Performance
The project evaluates multiple classification algorithms:
    • Gradient Boosting Trees
    • Logistic Regression
    • Decision Trees
    • Random Forest
    
Evaluation Metrics
    • Accuracy: Overall prediction correctness
    • F1-Score: Balance between precision and recall
    • AUC-ROC: Area under the receiver operating characteristic curve

  # 🔄 Workflow
    1. Data Loading: Load JSON data into Spark DataFrame
    2. Data Cleaning: Handle null values and filter invalid sessions
    3. EDA: Explore user behavior patterns and churn characteristics
    4. Feature Engineering: Create meaningful features for ML models
    5. Model Training: Train multiple classification algorithms
    6. Evaluation: Compare model performance and select best approach
    7. Results: Analyze feature importance and business insights
    
# 📈 Key Insights
    1. Behavioral Indicators: Users who churn tend to have:
        1. Lower total listening time
        2. More diverse song selection (higher distinct songs)
        3. Higher frequency of “Roll Advert” and “Thumbs Down” interactions 
        4.Fewer social interactions (less friend sharing)
    2. Temporal Patterns: Churned users typically have shorter engagement periods
    3. Feature Importance: Song interaction patterns and page visit frequencies are strong predictors

# 📁 Project Structure
sparkify-churn-prediction/
│
├── sparkify.ipynb          # Main analysis notebook
├── README.md                 # This file
├── data/                     # Data directory
│   └── mini_sparkify_event_data.json
└── models/                   # Saved models

    
📄 License
This project is part of a data science educational program and is available for learning purposes.
