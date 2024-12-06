# **Fitness Tracker with Sensor Data**

**Fitness Tracker with Sensor Data** is a machine learning-powered system designed to enhance workout tracking by analyzing motion data from sensors. It leverages advanced data processing, feature engineering, and predictive modeling to evaluate exercise form, classify workout types, and count repetitions. The project supports exercises like Squats, Bench Press, Deadlift, Overhead Press, and Barbell Row.

## **Key Features**

### 1. Exercise Classification  
The system identifies and categorizes exercises based on sensor data, achieving high accuracy through machine learning models such as Random Forests, SVM, and Neural Networks.  

### 2. Repetition Counting  
Tracks exercise repetitions using advanced signal processing techniques, ensuring accurate real-time performance monitoring.  

### 3. Posture Evaluation  
Provides feedback on form by analyzing motion and detecting improper postures, reducing the risk of injury.

### 4. Real-time Analysis  
Designed to work with wearable devices, enabling real-time tracking and insights during workouts.

---

## **How It Works**

### Data Processing
- **Cleansing**: Standardizes raw accelerometer and gyroscope data.  
- **Outlier Removal**: Employs methods like Interquartile Range (IQR) and Local Outlier Factor (LOF) to filter anomalies.

### Feature Engineering
- **Signal Transformation**: Applies low-pass filtering and Fourier Transformations for noise reduction and frequency analysis.  
- **Dimensionality Reduction**: Utilizes Principal Component Analysis (PCA) to enhance computational efficiency.  
- **Temporal Abstraction**: Captures trends across time intervals for better context.

### Predictive Modeling
- Trains machine learning algorithms to classify exercises and count repetitions accurately.  
- Optimizes model performance using hyperparameter tuning and cross-validation techniques.

---

## **Installation Instructions**

1. **Clone the Repository**  
   ```bash
   git clone https://github.com/Aishjahan/Fitness-Tracker-With-Sensor-Data.git
   cd Fitness-Tracker-With-Sensor-Data
   ```
2. Install dependencies from `requirements.txt` or `environment.yml`.
   ```bash
   pip install -r requirements.txt
   ```
3. Prepare the Dataset
Place raw sensor data in the designated directory and preprocess it by running the data processing scripts.


## **Usage Guide**

### Data Preparation

Run the `make_dataset.py` script to preprocess the raw sensor data:
```bash
python src/data/make_dataset.py
```

### Feature Engineering

Run `build_features.py` to create advanced features:
```bash
python src/features/build_features.py
```

### Model Training

Use `train_model.py` to train and optimize classification models:
```bash
python src/models/train_model.py
```

### Repetition Counting

Run `count_repetitions.py` to apply filters and count repetitions:
```bash
python src/features/count_repetitions.py
```

### Visualization

Generate workout and feature visualizations with `visualize.py`:
```bash
python src/visualization/visualize.py
```

## **Results and Analysis**

### Model Performance

The classification model achieves **98% accuracy**, offering highly reliable detection of exercise types and ensuring precise tracking of workout patterns for enhanced fitness insights.


## **Conclusion**

TrackFit AI leverages machine learning and sensor data to revolutionize personal fitness tracking by providing accurate exercise classification, posture correction, and repetition counting. With 98% accuracy in exercise recognition and advanced visualization tools, this project bridges the gap between technology and fitness. By promoting safe and effective workouts, TrackFit AI ensures users achieve their fitness goals with confidence. Future enhancements, such as integration with additional wearables and personalized feedback systems, will further elevate its utility and impact on the fitness community.
