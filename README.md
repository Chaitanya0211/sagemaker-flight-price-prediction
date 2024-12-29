# Flight Price Prediction Using AWS SageMaker

This project develops a machine learning model to predict flight prices based on various features such as airline, source, destination, departure time, arrival time, and more. The model is trained and deployed using AWS SageMaker, and a web application is built with Streamlit to provide an interactive interface for users.

## Project Overview

The objective of this project is to build a regression model that accurately predicts flight prices. By analyzing various factors that influence flight prices, the model can assist travelers, travel agencies, and airlines in making informed decisions.

## Dataset

The dataset used for this project contains information on flights, including:

- Airline
- Source
- Destination
- Departure Time
- Arrival Time
- Duration
- Total Stops
- Additional Information

## Data Preprocessing

Data preprocessing steps include:

1. **Handling Missing Values**: Removing or imputing missing data.
2. **Removing Whitespace**: Stripping unnecessary whitespace from strings.
3. **Standardizing Text**: Converting text to lowercase and standardizing formats.
4. **Converting Dates and Times**: Parsing dates and times into appropriate formats.
5. **Encoding Categorical Variables**: Transforming categorical variables into numerical representations.
6. **Normalizing Numerical Features**: Scaling numerical features for better model performance.

Pandas method chaining is employed throughout the preprocessing pipeline to ensure code readability and maintainability.

## Feature Engineering

Feature engineering involves creating new features that better represent the underlying patterns in the data. In this project, features such as the duration in minutes, departure hour, and arrival hour are extracted and used to enhance model performance. The `feature-engine` library is used for feature transformations, including:

- Handling missing data with imputation transformers.
- Encoding categorical variables using one-hot encoding.
- Scaling numerical features.

## Model Training

The model is trained using AWS SageMaker and the XGBoost algorithm, leveraging SageMaker’s scalable infrastructure. The training process includes:

- **Selecting Algorithms**: Using XGBoost for regression tasks.
- **Hyperparameter Tuning**: Optimizing model parameters such as learning rate, max depth, and number of estimators.
- **Cross-Validation**: Validating the model to prevent overfitting.

## Model Deployment

After training, the model is deployed using AWS SageMaker's deployment services, allowing it to be accessed for real-time predictions.

## Web Application

A web application is built using Streamlit to provide an interactive interface where users can input flight details and receive price predictions. The app is deployed on Streamlit Cloud for accessibility.

## Getting Started

To get a local copy up and running, follow these steps:

### Prerequisites

- Python 3.6 or higher
- AWS Account with SageMaker access
- Streamlit Account for deployment

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/Chaitanya0211/sagemaker-flight-price-prediction.git
   ```

2. Navigate to the project directory:

   ```bash
   cd sagemaker-flight-price-prediction
   ```

3. Install the required packages:

   ```bash
   pip install -r requirements.txt
   ```

## Dependencies

The project requires the following Python packages:

- pandas
- numpy
- scikit-learn
- xgboost
- streamlit
- boto3
- feature-engine

These can be installed using the `requirements.txt` file provided in the repository.

## Usage

1. **Data Preparation**: Ensure the dataset is available in the `Data` directory.
2. **Model Training**: Use the Jupyter notebooks in the `Code_Files` directory to preprocess data, engineer features, and train the model using AWS SageMaker.
3. **Model Deployment**: Deploy the trained model using AWS SageMaker's deployment services.
4. **Web Application**: Run the Streamlit app locally:

   ```bash
   streamlit run app.py
   ```

   Or deploy it on Streamlit Cloud for public access.

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

