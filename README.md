# 30 Days DevOps Challenge - Weather Dashboard
Day 1: Building a weather data collection system using AWS S3 and OpenWeather API

## Features
- Fetch real-time weather data using the OpenWeather API.
- Store weather data securely in an AWS S3 bucket.
- Ensure unique bucket names with random number generation for naming.

Prerequisites
Before running this project, make sure you have the following:
- Python 3.8+ installed
- An OpenWeather API key (sign up [here](https://openweathermap.org/api)) 
- AWS CLI configured with an IAM user having S3 permissions ([Set up AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html)) 

## Setup and Installation
1. **Clone the Repository from [Shae's repository](https://github.com/ShaeInTheCloud)**  
   ```sh  
   git clone https://github.com/ShaeInTheCloud/30days-weather-dashboard.git  
   cd 30days-weather-dashboard

2. **Set Up a Virtual Environment**
    ```sh
    python -m venv venv  
    source venv/bin/activate  # For Windows: venv\Scripts\activate

3. **Install Dependencies**
     ```sh
    pip install -r requirements.txt  

5. **Add Your API Key and Configuration**
 - Create a .env file in the root directory:
  ```sh
  OPENWEATHER_API_KEY==<your_openweather_api_key>  
  AWS_BUCKET_NAME==<unique-bucket-name> (if you are seeing error while creating the bucket, you might need to change the name here. No underscore. You can use camelCase pattern)

```
---
## How It Works

1. The application sends a GET request to the OpenWeather API to retrieve weather data for a specific location.
2. The data is saved to an AWS S3 bucket.
3. To avoid bucket name conflicts, a random number is appended to the bucket prefix.

***Running the Application***
Run the script:
  ```sh
   python app.py
```
![image](https://github.com/user-attachments/assets/47c8985f-b864-4cd2-98dd-897836854623)


