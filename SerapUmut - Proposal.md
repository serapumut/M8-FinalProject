# SerapUmut - Final Capstone Project Proposal Outline
Final Project Proposal document. 

## I. Introduction

- The project, titled “Player Retention Prediction for Video Games,” focuses on developing a machine learning model to predict whether a player will return to a video game after their first session.
- This project falls under the deployed predictive model category, as it involves creating a trained machine learning model and deploying it with a user-friendly interface.
- This project will include an interactive and user-friendly deployment using Streamlit, a platform that simplifies app development and enhances user engagement.

## II. Project Objective

- The primary goal of this project is to predict player retention, helping game developers and publishers understand player behavior and improve engagement strategies.
- The problem being addressed is how to identify the factors influencing a player’s likelihood of returning to a game, allowing for better-targeted interventions like personalized incentives or game design adjustments.
  
## III. Data Description

- Data Source:
  - The dataset will be collected using the RAWG Video Games Database API, which provides detailed game-related information, including player ratings, release dates, genres, and platforms.
  - An API key has already been obtained for data access.
- Data Structure:
  - Game Metrics: Ratings, release dates, genres, and platforms.
  - Player Metrics: Session duration and other engagement factors (to be integrated based on analysis).
- Data Collection Strategy:
  - Use the /games endpoint to retrieve data on popular and recently released games.
  - Implement request parameters for filtering (e.g., ordering by popularity and rating).
  - Handle missing or incomplete data by replacing null values or augmenting with derived metrics.
- Data Format:
  - Data will be saved in CSV format for preprocessing and analysis.
- API Usage Example:
  - Data will be collected programmatically using Python, with requests sent to the RAWG API endpoints, such as:
    - GET https://api.rawg.io/api/games?key={myKEY}&page=1&page_size=10

## IV. Methodology

- Data Collection and Preprocessing:
  - Retrieve game data using the RAWG API.
  - Clean and preprocess the data (handle missing values, normalize features, encode categorical variables).
- Model Development:
  - Use machine learning classification algorithms (e.g., Random Forest, Neural Networks) to predict player retention.
  - Evaluate models using metrics such as accuracy, precision, recall, and F1-score, particularly addressing imbalanced data.
- Deployment:
  - Deploy the model using Streamlit, an interactive platform for building and hosting applications.
  - Include dynamic components like sliders, dropdown menus, and text inputs for user data entry.
  - Display visualizations such as retention probability graphs, feature importance charts, and performance metrics.
- Scalability:
  - Plan for larger datasets by optimizing data preprocessing and modeling pipelines.
  - Ensure the app can be updated easily with additional features or retrained models using Streamlit's modular architecture.

## V. Expected Deliverables

- Trained Predictive Model:
  - A saved model capable of predicting player retention for new data.
- Deployed Streamlit Application:
  - A user-friendly interface with dynamic components for data input and real-time visual outputs, including:
    - Retention probability graphs.
    - Feature importance charts.
    - Performance metrics (accuracy, precision, recall, and F1-score).
- Documentation:
  - A GitHub repository containing scripts for data collection, model training, and app deployment, with a comprehensive README.md file.

## VI. Timeline and Tasks

- Days	   Task
  - 1-2     Data collection via RAWG API
  - 1–2	   Data collection via RAWG API
  - 3–4	   Data preprocessing and cleaning
  - 5–6	   Model training and evaluation
  - 7–9	   Develop Streamlit app with dynamic components
  - 10–12	 Add visualizations and performance metrics
  - 13–14	 Test and host the app on Streamlit Community Cloud
  - 15–16	 Final testing and preparation for presentation
  
## VII. Potential Challenges

- API Rate Limits:
  - Solution: Implement request throttling and batch processing to avoid exceeding limits.
- Incomplete Data:
  - Solution: Use fallback strategies like imputing missing values or excluding incomplete records.
- Scalability of the App:
  - Solution: Use Streamlit’s modular design to ensure scalability for larger datasets and enable periodic retraining with updated data.
- Deployment Issues:
  - Solution: Host the app on Streamlit Community Cloud for accessibility and ensure robust local testing before deployment.
