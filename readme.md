
project_folder/
│
├── Analytics/                                # Contains scripts for analyzing model performance
│   └── model_analytics.py                    # Script for model analytics
│
├── Data/                                     # Directory for datasets
│   ├── 1_raw/                                # Raw data files
│   │   ├── apartments.csv                    # Dataset of apartments
│   │   ├── flats.csv                         # Dataset of flats
│   │   ├── houses.csv                        # Dataset of houses
│   │   └── latlong.csv                       # Dataset containing latitude and longitude data
│   │
│   ├── 2_merged/                             # Merged datasets
│   │   └── data_merged.csv                   # Merged data file
│   │
│   ├── 3_processed/                          # Processed data files
│   │   ├── test_processed.csv                # Processed test dataset
│   │   └── train_processed.csv               # Processed training dataset
│   │
│   ├── 4_feature_engineering/                # Feature engineering outputs
│   │   ├── 1_feature_extracted/              # Extracted features
│   │   │   ├── test_extracted.csv            # Extracted features for the test set
│   │   │   └── train_extracted.csv           # Extracted features for the training set
│   │   │
│   │   └── 2_interim/                        # Interim features
│   │       ├── test_interim.csv              # Interim features for the test set
│   │       └── train_interim.csv             # Interim features for the training set
│   │
│   ├── 5_outlier_treated/                    # Outlier treated data
│   │   ├── test_outlier_treated.csv          # Outlier treated test dataset
│   │   └── train_outlier_treated.csv         # Outlier treated training dataset
│   │
│   ├── 6_missing_value_imputed/              # Missing value imputed datasets
│   │   ├── test_missing_value_imputed.csv    # Imputed missing values for test set
│   │   └── train_missing_value_imputed.csv   # Imputed missing values for training set
│   │
│   ├── 7_feature_selected/                   # Final selected features
│   │   ├── test_feature_selected.csv         # Selected features for the test set
│   │   └── train_feature_selected.csv        # Selected features for the training set
│   │
│   └── 8_analytics/                          # Analytics data
│       └── data_analytics.csv                # Final analytics dataset
│
├── ETL_Pipeline/                             # ETL pipeline configuration
│   ├── airflow_paths.yaml                    # Airflow paths configuration
│   ├── airflow_pipeline.py                   # Airflow pipeline script
│   ├── etl_config.yaml                       # ETL pipeline configuration
│   ├── etl.log                               # ETL log file
│   └── logging_utils.py                      # Logging utilities
│
├── Machine_Learning_Pipeline/                # Machine learning pipeline components
│   ├── best_hyperparameters.json             # Best hyperparameters from training
│   ├── kubeflow_paths.yaml                   # Kubeflow paths configuration
│   ├── kubeflow_pipeline.py                  # Kubeflow pipeline script
│   ├── ml_config.yaml                        # Machine learning pipeline configuration
│   ├── ml.log                                # Machine learning log file
│   └── params.yaml                           # Parameters configuration file
│
├── models/                                   # Trained models
│   ├── cosine_sim_facilities.pkl             # Model for cosine similarity based on facilities
│   ├── cosine_sim_features.pkl               # Model for cosine similarity based on features
│   ├── dataset.pkl                           # Dataset for model training
│   ├── feature_text.pkl                      # Feature text processing model
│   ├── location_matrix.pkl                   # Model for location matrix
│   ├── price_predictor.pkl                   # Trained price predictor model
│
├── src/                                      # Source code for various stages of the pipeline
│   ├── 1_Data_Ingestion/                     # Scripts for data ingestion
│   │   ├── apartments.py                     # Data ingestion for apartments
│   │   ├── flats.py                          # Data ingestion for flats
│   │   ├── houses.py                         # Data ingestion for houses
│   │   └── latlong.py                        # Data ingestion for latitude and longitude
│   │
│   ├── 2_Data_Preprocessing/                 # Data preprocessing scripts
│   │   ├── data_merging.py                   # Script for data merging
│   │   └── data_cleaning.py                  # Script for data cleaning
│   │
│   ├── 3_Feature_Engineering/                # Scripts for feature engineering
│   │   ├── feature_extraction.py             # Script for feature extraction
│   │   └── feature_interim.py                # Script for interim feature engineering
│   │
│   ├── 4_Anomaly_Detection/                  # Scripts for anomaly detection
│   │   └── outlier_treatment.py              # Script for outlier treatment
│   │
│   ├── 5_Missing_Value_Imputation/           # Scripts for missing value imputation
│   │   └── missing_value_imputation.py       # Script for missing value imputation
│   │
│   ├── 6_Feature_Selection/                  # Scripts for feature selection
│   │   └── feature_selection.py              # Script for feature selection
│   │
│   ├── 7_Model_Training/                     # Scripts for model training
│   │   ├── price_predictor_model.py          # Script for training price predictor model
│   │   └── property_recommender_model.py     # Script for training property recommender model
│
├── webpage/                                  # Web application components
│   ├── 1_Price_Predictor.py                  # Price prediction web app
│   ├── 2_Analysis_App.py                     # Analysis web app
│   ├── 3_Recommend_Appartments.py            # Apartment recommendation web app
│   ├── 4_Home.py                             # Home page for the web app
│   └── background.jpg                        # Background image for the web app
│
└── project_flow_structure.md                 # Project flow structure documentation

To run the website go to the webpage folder and run this command in terminal-> streamlit run 4_Home.py