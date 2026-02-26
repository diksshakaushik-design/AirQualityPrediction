# Air Quality Prediction

This project predicts **Air Quality Index (AQI)** for a city using historical data and Random Forest regression. It also includes a **color-coded alert system** for the next 7 days, indicating air quality levels from "Good" to "Hazardous".

---

## **Features**

1. **Data Preprocessing**
   - Handles missing values (`ffill`) for AQI, Status, and Country.
   - Encodes categorical features like `Status` and `Country`.
   - Extracts date-based features (`day`, `month`, `year`) for prediction.

2. **Machine Learning Models**
   - **Linear Regression** for baseline AQI prediction.
   - **Random Forest Regressor** for accurate prediction of AQI.

3. **Time-Series Prediction**
   - Creates **lag features** using the past 7 days to predict the next day.
   - Predicts **next 7 days AQI** recursively.

4. **Color-Coded Alerts**
   - Classifies predicted AQI into categories:
     - **Good (0–50)** → Green
     - **Moderate (51–100)** → Yellow
     - **Unhealthy (101–200)** → Orange
     - **Very Unhealthy (201–300)** → Red
     - **Hazardous (301+)** → Purple
   - Visualizes predictions with a **bar chart** and category labels.

---

## **Dependencies**

- Python 3.x  
- pandas  
- numpy  
- matplotlib  
- scikit-learn  

Install dependencies with:

```bash
pip install pandas numpy matplotlib scikit-learn