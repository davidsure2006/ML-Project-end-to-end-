# **End-to-End Machine Learning Project**  
*A Complete Machine Learning Pipeline for California Housing Price Prediction*  

## **Overview**  
This project implements a full machine learning workflow to predict California housing prices based on location and housing attributes. It covers data preprocessing, model training, evaluation, and deployment using Flask and Docker.  

## **Features**  
- **Data Preprocessing Pipeline** – Handles missing values, categorical encoding, and feature scaling for clean data.  
- **Machine Learning Models** – Implements regression models, including Linear Regression, Decision Trees, and Ensemble methods for performance comparison.  
- **Model Evaluation System** – Uses cross-validation, confusion matrices, and precision-recall metrics to assess accuracy and generalization.  
- **REST API Deployment** – Deploys the trained model via Flask and Docker, enabling real-time predictions.  
- **Automated Workflows** – Implements logging, error handling, and parameter tuning for a robust system.  

## **Dataset**  
The project uses the **California Housing Prices dataset**, which contains information about different housing attributes such as median income, number of rooms, and location coordinates to predict median house values.  

## **Installation**  
1. Clone the repository:  
   ```bash
   git clone https://github.com/davidsure2006/ML-Project-end-to-end-.git
   cd end-to-end-ml-project
   ```  
2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```  
3. Run the application:  
   ```bash
   python app.py
   ```  

## **API Usage**  
Once the Flask server is running, you can send a POST request to get predictions:  
```bash
curl -X POST http://127.0.0.1:5000/predict -H "Content-Type: application/json" -d '{
    "median_income": 3.5,
    "total_rooms": 1500,
    "housing_median_age": 20,
    "latitude": 34.05,
    "longitude": -118.25
}'
```  
Response:  
```json
{
    "predicted_price": 280000
}
```  

## **Deployment**  
To deploy with Docker:  
1. Build the Docker image:  
   ```bash
   docker build -t housing-price-predictor .
   ```  
2. Run the container:  
   ```bash
   docker run -p 5000:5000 housing-price-predictor
   ```  

## **Future Improvements**  
- Enhance model performance with hyperparameter tuning.  
- Integrate a frontend dashboard for visualization.  
- Deploy using cloud services like AWS or GCP.  

---

