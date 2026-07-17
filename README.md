# BritishAirways_Simulation
# ✈️ Airline Customer Booking Prediction

An end-to-end data processing and Exploratory Data Analysis (EDA) pipeline designed to predict airline customer booking completions. This project analyzes customer behavior—such as baggage preferences, flight days, channels of booking, and length of stay—to identify key factors driving completed reservations.

---

## 📊 Dataset Overview
The project processes a dataset of **50,000 passenger booking records** containing 14 key behavioral and flight features:

| Feature Name | Description |
| :--- | :--- |
| `num_passengers` | Number of passengers in the booking |
| `sales_channel` | Channel used to book (Internet, Mobile) |
| `trip_type` | Booking trip type (RoundTrip, OneWay, CircleTrip) |
| `purchase_lead` | Number of days between booking date and travel date |
| `length_of_stay` | Total days of stay at the destination |
| `flight_hour` | Hour of the flight departure |
| `flight_day` | Day of the week of the flight |
| `route` | Origin to destination route path |
| `booking_origin` | Country of booking origin |
| `wants_extra_baggage` | Binary indicator (1 if opted for extra baggage, else 0) |
| `wants_preferred_seat` | Binary indicator (1 if opted for preferred seat, else 0) |
| `wants_in_flight_meals` | Binary indicator (1 if opted for in-flight meals, else 0) |
| `flight_duration` | Duration of flight in hours |
| `booking_complete` | **Target Variable** (1 if booking completed, else 0) |

---

## 🛠️ Data Preprocessing & Cleaning Pipeline
To make the raw data suitable for machine learning models, the following cleaning steps are implemented in the notebook:

1. **Null Values Check:** Confirmed zero missing data across all 14 features.
2. **De-duplication:** Identified and removed **719 duplicate records**, reducing the dataset size from 50,000 to **49,281 unique rows**.
3. **Categorical Mapping:** 
   * Mapped `flight_day` names (`Mon`, `Tue`... `Sun`) to numerical values (`1` to `7`).
4. **Categorical Encoding:** 
   * Converted textual categories to numerical codes using category codes (`.cat.codes`) for features: `sales_channel`, `trip_type`, `route`, and `booking_origin`.

---

## 🚀 Getting Started

### Prerequisites
Make sure you have Python installed, along with the following libraries:
```bash
pip install pandas numpy matplotlib seaborn
Clone this repository:

Bash
git clone [https://github.com/YOUR_USERNAME/airline-booking-prediction.git](https://github.com/YOUR_USERNAME/airline-booking-prediction.git)
cd airline-booking-prediction
Open the notebook in your environment (Jupyter / VS Code / Google Colab).

Upload the customer_booking.csv dataset when prompted.

Execute the cells sequentially to run the preprocessing pipeline.

📈 Next Steps & Roadmap
[ ] EDA Visualizations: Build Correlation Heatmaps, Booking Status distributions, and Feature Importance plots.

[ ] Handling Class Imbalance: Address target class distribution skewness (only ~15% bookings completed).

[ ] Machine Learning Model: Train classifiers like XGBoost or Random Forest to predict booking_complete.

🤝 Contributing
Contributions are welcome! If you want to add machine learning models or improve visualizations, feel free to fork this repo and submit a PR.


---

### Key Highlights of this README:
* **Feature Table:** Ekdum clean formatting mein columns ke descriptions.
* **Pipeline Explanation:** Notebook mein tumne jo duplicates handle kiye aur mapping/encoding ki, uski clean summary.
* **Quick Start Guide:** Repo setup karne aur run karne ke code snippets.
