# Wafer Fault Detection
![Python](https://img.shields.io/badge/Python-3.7%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-2.0%2B-green?style=for-the-badge&logo=flask&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white)


## 📌 Project Overview

*   **Reduce Costs**: Minimizing waste of expensive materials.
*   **Improve Yield**: Ensuring a higher percentage of usable chips.
*   **Optimize Process**: Providing feedback to adjust manufacturing parameters.

This application automates the detection process using sensor data. It employs a robust pipeline that handles data ingestion, validating raw data streams, preprocessing (including handling missing values and scaling), and applying advanced clustering techniques to group similar data patterns. For each cluster, the system dynamically selects and tunes the best-performing machine learning model (such as Random Forest or XGBoost) to predict whether a wafer is "Good" or "Bad" with high accuracy.

The solution is wrapped in a user-friendly Flask web application, allowing operators to easily upload data batches and receive instant prediction reports.

## 🚀 Key Features

*   ** Automated Data Validation**: rigoros checks for schema compliane, file name formats, and data integrity.
*   **Intelligent Preprocessing**: 
    *   Automated handling of missing values using KNN imputation.
    *   Dimensionality reduction by removing low-variance features.
*   **Advanced ML Pipeline**: 
    *   **Clustering**: Utilizes **K-Means** to segment data, handling data heterogeneity.
    *   **Dynamic Model Selection**: Trains multiple models (Random Forest, XGBoost) for *each* cluster and selects the one with the best AUC score.
*   **Web Interface**: Intuitive UI built with Bootstrap for easy interaction.
*   **Robust Logging**: Detailed logs for every step of the pipeline (Training, Prediction, DB operations) to aid debugging and auditing.
*   **Scalable Architecture**: Modular code structure allowing for easy maintenance and scalability.


## 🛠️ Technology Stack

*   **Programming Language**: Python
*   **Web Framework**: Flask
*   **Machine Learning Libraries**: Scikit-Learn, XGBoost, Kneed
*   **Data Processing**: Pandas, NumPy
*   **Database**: SQLite (for lightweight, serverless data storage)
*   **Frontend**: HTML5, CSS3, Bootstrap 4

## 📂 Project Structure

```
WaferFaultDetection/
├── application_logging/    # Custom logging modules for tracking app events
├── best_model_finder/      # Logic for model selection and hyperparameter tuning
├── data_ingestion/         # Modules for reading and loading data
├── data_preprocessing/     # Data cleaning, transformation, and clustering
├── DataTransform_Training/ # formatting training data
├── DataTransformation_Prediction/ # Formatting prediction data
├── DataTypeValidation_Insertion_Training/ # Schema validation & DB insertion (Training)
├── DataTypeValidation_Insertion_Prediction/ # Schema validation & DB insertion (Prediction)
├── file_operations/        # Saving and loading trained models
├── models/                 # specific directory for saving models
├── templates/              # HTML templates for the web interface
├── main.py                 # Application entry point (Flask App)
├── trainingModel.py        # Driver script for the training pipeline
├── predictFromModel.py     # Driver script for the prediction pipeline
├── requirements.txt        # Python dependencies
└── ...
```

## ⚙️ Installation

1.  **Clone the repository**:
    ```bash
    git clone https://github.com/your-username/WaferFaultDetection.git
    cd WaferFaultDetection
    ```

2.  **Create a virtual environment** (recommended):
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```

3.  **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

## 🏃 Usage

1.  **Start the Server**:
    ```bash
    python main.py
    ```

2.  **Open Web App**:
    Go to `http://localhost:5000` in your web browser.

3.  **Predict**:
    *   Upload a folder or file containing wafer sensor data (CSV format).
    *   Click "Predict" to run the pipeline.
    *   Download the detailed prediction report.

## ✍️ Author
**[Arnab Ghosh]**

*   **GitHub Profile**: [https://github.com/Arnab-Ghosh7](https://github.com/Arnab-Ghosh7)


## 🤝 Contribution
Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/Arnab-Ghosh7/WaferFaultDetection/issues).



## 📄 License
This project is licensed under the [GNU License](LICENSE).
