# IPL-2025-Winner-Prediction

## Overview
This project predicts the winners of IPL (Indian Premier League) 2025 matches using machine learning. The model is trained on historical IPL match data from 2008-2024 and applies machine learning algorithms to predict outcomes of upcoming matches in the IPL 2025 season.

## Features
- Historical IPL match data analysis (2008-2024)
- Machine learning model to predict match outcomes
- Predictions for upcoming IPL 2025 matches
- Analysis of team performances and winning probabilities

## Dataset
The project uses the following datasets:
- **matches.csv / matches_24.csv**: Historical match data from 2008-2024 seasons
- **deliveries.csv**: Ball-by-ball data for matches
- **IPL_2025_SEASON_SCHEDULE.csv**: Schedule for the upcoming IPL 2025 season

## Technologies Used
- Pandas for data manipulation
- NumPy for numerical operations
- Scikit-learn for machine learning models
- Matplotlib and other plotting libraries for visualization
- Jupyter Notebook for interactive development

## Model
The project implements several machine learning models, including:
- Decision Tree
- Gradient Boosting Classifier
- XGBoost
- Random Forest

Based on testing, the Gradient Boosting Classifier was selected for the final prediction model, trained on historical match data with features like team performance, venue statistics, toss outcomes, and other relevant match variables.

## Files in Repository
- **Ipl_25.ipynb**: Jupyter notebook with all the code, data analysis, model training and predictions
- **matches_24.csv**: Historical match data up to 2024
- **archive/matches.csv**: Original historical match data
- **archive/deliveries.csv**: Ball-by-ball data for historical matches
- **IPL_2025_SEASON_SCHEDULE.csv**: Schedule of IPL 2025 matches
- **best_gbc_model.pkl**: Serialized trained model for predictions

## Setup and Usage
1. Clone the repository:
   ```
   git clone https://github.com/yourusername/IPL-2025-Winner-Prediction.git
   cd IPL-2025-Winner-Prediction
   ```

2. Install dependencies:
   ```
   pip install pandas numpy scikit-learn xgboost matplotlib seaborn jupyter
   ```

3. Run the Jupyter notebook:
   ```
   jupyter notebook Ipl_25.ipynb
   ```

4. To make predictions for new matches, you can either:
   - Run the prediction cells in the notebook
   - Load the serialized model:
     ```python
     import pickle
     with open('best_gbc_model.pkl', 'rb') as f:
         model = pickle.load(f)
     # Prepare your features and make predictions
     predictions = model.predict(X_new)
     ```


## Future Improvements
- Incorporate player-specific data for more nuanced predictions
- Add weather data as it affects match outcomes
- Implement a web interface for real-time predictions
- Include social media sentiment analysis as an additional feature