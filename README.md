30 Days DevOps Challenge - Weather Dashboard
Day 1: Building a weather data collection system using AWS S3 and OpenWeather API

Weather Data Collection System - DevOps Day 1 Challenge

Features
Fetch real-time weather data using the OpenWeather API.

Store weather data securely in an AWS S3 bucket.

Ensure unique bucket names with random number generation for naming.

Prerequisites
Before running this project, make sure you have the following:

Python 3.8+ installed
An OpenWeather API key (sign up here)
AWS CLI configured with an IAM user having S3 permissions (Set up AWS CLI)

Setup and Installation
Clone the Repository from Shae's repository
git clone https://github.com/ShaeInTheCloud/30days-weather-dashboard.git  
cd 30days-weather-dashboard
Set Up a Virtual Environment
python -m venv venv  
source venv/bin/activate  # For Windows: venv\Scripts\activate
Install Dependencies
pip install -r requirements.txt  
Add Your API Key and Configuration
Create a .env file in the root directory:

OPENWEATHER_API_KEY==<your_openweather_api_key>  
AWS_BUCKET_NAME==<unique-bucket-name>

How It Works
The application sends a GET request to the OpenWeather API to retrieve weather data for a specific location.
The data is saved to an AWS S3 bucket.
To avoid bucket name conflicts, a random number is appended to the bucket prefix.
Running the Application Run the script:

 python app.py
