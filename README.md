# 💻 Laptop Price Predictor

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://groupx-minimodel.streamlit.app/)

This project is a machine learning-powered web application that predicts the price of laptops based on their technical specifications. The model is trained on a dataset of laptop prices and deployed as an interactive web app using Streamlit.

## 📖 Table of Contents
- [About the App](#-about-the-app)
- [Live Demo](#-live-demo)
- [Built By](#-built-by)
- [How to Use](#-how-to-use)
- [Project Workflow](#-project-workflow)
  - [Exploratory Data Analysis (EDA)](#1-exploratory-data-analysis-eda)
  - [Feature Engineering & Data Preprocessing](#2-feature-engineering--data-preprocessing)
  - [Model Training](#3-model-training)
- [Deployment](#-deployment)
  - [Saving Model Artifacts](#saving-model-artifacts)
  - [Deploying to Streamlit Cloud](#deploying-to-streamlit-cloud)
- [Technologies Used](#-technologies-used)
- [Support Us](#-support-us)

## 📝 About the App

The Laptop Price Predictor is an intuitive tool designed to provide estimated prices for laptops. Users can input various specifications, such as screen size, RAM, storage, brand, and type, and the application will return a predicted price in Euros and US Dollars. The app also features a detailed sidebar with instructions, project information, and quick tips for users.

## 🚀 Live Demo

The application is deployed and accessible online via Streamlit Cloud.

**Live App Link:** [**https://groupx-minimodel.streamlit.app/**](https://groupx-minimodel.streamlit.app/)

**Documuentation** [**Click Here**](https://docs.google.com/document/d/1EQ4x4KCKcaqqYGS836xwhlEjp7mTcI8T1BVkU4aopYU/edit?usp=sharing)

## 👨‍💻 Built By

This project was developed by a team of dedicated Computer Engineering students from **Group X**.

| Name          | GitHub Profile                                                |
|---------------|---------------------------------------------------------------|
| **Tom Udoh** | [Link to Profile](https://github.com/tomdan-ai)                |
| **Bez-01** | [Link to Profile](https://github.com/Bez-01)                     |
| **Datoiyoabasi** | [Link to Profile](https://github.com/datoiyoabasi92-lgtm)  |
| **Etimbukedem** | [Link to Profile](https://github.com/Etimbukedem)           |
| **Noble** | [Link to Profile](https://github.com/noble1999)                   |
| **Steve Bruce** | [Link to Profile](https://github.com/SteveBruce7)           |
| **Vemah** | [Link to Profile](https://github.com/vemah619-bot)                |
| **Aniebiet Jack** | [Link to Profile](https://github.com/Yuto-xyz)            |

## 🛠️ How to Use

To run this project locally, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/tomdan-ai/mini_model.git
    cd mini_model
    ```

2.  **Create and activate a virtual environment:**
    ```bash
    python -m venv venv
    .\venv\Scripts\activate  # On Windows
    # source venv/bin/activate  # On macOS/Linux
    ```

3.  **Install the required dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Run the Streamlit application:**
    ```bash
    streamlit run streamlit_app.py
    ```

The application will open in your default web browser.

## 📈 Project Workflow

The project was developed in a Jupyter Notebook (`laptop_price.ipynb`), where all data analysis, preprocessing, and model training were performed.

### 1. Exploratory Data Analysis (EDA)

The initial phase involved a deep dive into the `laptop_price.csv` dataset to understand its structure, identify patterns, and uncover insights. Key steps included:
-   **Data Loading & Initial Inspection:** Loaded the dataset and examined its shape, columns, and data types.
-   **Data Cleaning:** Handled missing values and corrected data inconsistencies.
-   **Univariate & Bivariate Analysis:** Analyzed individual features and their relationships with the target variable (Price). Visualizations like histograms, bar charts, and scatter plots were used to explore distributions and correlations.
-   **Key Insights:** Identified strong correlations between price and features like RAM, CPU, and storage type (SSD vs. HDD).

### 2. Feature Engineering & Data Preprocessing

To prepare the data for modeling, several feature engineering and preprocessing steps were taken:
-   **Feature Extraction:** Created new features like `Storage_Size_GB`, `Pixels`, `X_res`, and `Y_res` from existing columns to provide more meaningful inputs to the model.
-   **Categorical Encoding:** Applied One-Hot Encoding to convert categorical features (e.g., `Company`, `TypeName`, `Storage_Type`) into a numerical format.
-   **Feature Scaling:** Used `StandardScaler` to scale numerical features, ensuring that all features contribute equally to the model's training process.

### 3. Model Training

A **Linear Regression** model was chosen for its simplicity and interpretability.
-   The preprocessed data was split into training and testing sets.
-   The model was trained on the training data.
-   The model's performance was evaluated on the test set, and it demonstrated reliable predictive accuracy for this regression task.

## 📦 Deployment

### Saving Model Artifacts

After training, the essential components for prediction were saved as pickle files:
-   `laptop_price_model.pkl`: The trained Linear Regression model.
-   `scaler.pkl`: The `StandardScaler` object used for feature scaling.
-   `feature_names.pkl`: The list of one-hot encoded feature names required for creating the input DataFrame in the app.

### Deploying to Streamlit Cloud

The application is deployed on Streamlit Cloud, which provides a seamless way to share Streamlit apps. The deployment process involves:
1.  Pushing the entire project (including `streamlit_app.py`, `requirements.txt`, and the `.pkl` files) to the GitHub repository.
2.  Connecting the GitHub repository to a new app in the Streamlit Cloud dashboard.
3.  Configuring the main file path to `streamlit_app.py`.
4.  Deploying the app. Streamlit Cloud automatically installs the dependencies from `requirements.txt` and runs the application.

## 💻 Technologies Used

-   **Programming Language:** Python
-   **Data Analysis & ML:** Pandas, NumPy, Scikit-learn
-   **Web Framework:** Streamlit
-   **Development Environment:** Jupyter Notebook, VS Code
-   **Deployment:** Streamlit Cloud, Git & GitHub

## ⭐ Support Us

If you find this project helpful or interesting, please consider giving it a star on GitHub! Your support is greatly appreciated and motivates us to continue creating
