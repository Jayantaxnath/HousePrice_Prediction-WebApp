# 🏡 House Price Prediction Web App

![Web UI](https://github.com/user-attachments/assets/2017aa52-96ff-4d38-b4d2-21c7bb91e4d6)


## 📌 About the Project

The **House Price Prediction Web App** is a Flask-based machine learning application that estimates house prices based on user inputs like:
- ✅ BHK (Bedrooms)
- ✅ Bathrooms
- ✅ Area (sqft)
- ✅ Location

It utilizes a trained ML model to provide accurate predictions, making it useful for buyers, sellers, and real estate analysts.

---

## 📂 Project Structure

HousePrice_Prediction-WebApp
│── model
│   ├── banglore_home_prices_final.ipynb    # Jupyter notebook for model training
│   ├── banglore_home_prices_model.pickle   # Trained ML model
│   ├── bengaluru_house_prices.csv          # Dataset used for training
│   ├── columns.json                        # Stores column names like bhk, bath, area, locations.
│
│── server
│   ├── __pycache__/                         # Cached Python files
│   ├── model_data/
│   │   ├── banglore_home_prices_model.pickle   # Model used in deployment
|   |   ├── columns.json                        # Stores column names for model inference
│   ├── requirements.txt                       # Dependencies and required packages
│   ├── server.py                               # Main Flask API to handle requests
│   ├── util.py                                 # Utility functions for processing requests
│
│── web_ui
│   ├── app.html        # HTML file for the web interface
│   ├── app.css         # CSS file for styling
│   ├── app.js          # JavaScript file to handle frontend interactions
│   ├── image.png       # Web UI-related images
│

## 🎯 How It Works

1️⃣ **User inputs** house details like BHK, bathrooms, area (sqft), and location in the web interface.
2️⃣ The details are sent to the Flask **server (server.py)**.
3️⃣ **Trained ML model** processes the input and makes predictions.
4️⃣ The predicted price is displayed on the web UI dynamically.

## 🛠 Tech Stack

- **Frontend**: HTML, CSS, JavaScript
- **Backend**: Flask (Python)
- **Machine Learning**: Scikit-learn, Pandas, NumPy
- **Model Storage**: Pickle

## 📂 Step-by-Step Explanation of the Project

### 1️⃣ Data Collection & Preprocessing
- The dataset (**bengaluru_house_prices.csv**) contains house price data for Bangalore.
- It is **cleaned, processed, and used to train a Machine Learning model**.

### 2️⃣ Training the Machine Learning Model
- The **Jupyter Notebook (banglore_home_prices_final.ipynb)** is used for model training.
- **Data preprocessing**: Handling missing values, encoding categorical variables, and feature selection.
- **Training** a Linear Regression model on the dataset.
- **Saving the trained model** using Pickle (**banglore_home_prices_model.pickle**).

### 3️⃣ Setting Up the Flask Server
- The **Flask app (server.py)** receives HTTP requests from the frontend.
- It **loads the trained ML model** and predicts the house price.
- **Utility functions (util.py)** process incoming requests and extract required features.

### 4️⃣ Creating the Frontend (Web UI)
- **app.html**: Provides the user interface.
- **app.css** styles the UI.
- **app.js** handles frontend interactions.
- **image assets** enhance user experience.

### 5️⃣ Running the Web App

#### 1. Clone the Repository
```bash
git clone https://github.com/repo-name.git
```

#### 2. Create a Virtual Environment (Recommended)
```sh
python -m venv venv
source venv/bin/activate  # For Mac/Linux
venv\Scripts\activate   # For Windows
```

#### 3. Install Dependencies
```sh
pip install -r server/requirements.txt
```

#### 4. Run the Flask Server
```sh
python server/server.py
```
- The API will be available at **http://127.0.0.1:5000/**

#### 5. Open the Web UI
Simply open **web_ui/app.html** in your browser.

## 🔮 Future Enhancements

✅ Adding more features like:
- Amenities
- Neighborhood rating
- Property age

✅ Improving **UI/UX** for a better user experience.

✅ **Deploying the app** using cloud platforms like AWS, Heroku, or Google Cloud.

---
Made with ❤️ for House Price Prediction!
