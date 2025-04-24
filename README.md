📡 Google Smartphone Decimeter Challenge 2023–2024
This repository contains a complete solution pipeline for the Google Smartphone Decimeter Challenge (GSDC) 2023–2024, a competition hosted on Kaggle and supported by Google Research.
The challenge revolves around improving smartphone positioning accuracy using raw GNSS (Global Navigation Satellite System) data, which is often impacted by noise, multipath errors, and urban obstructions.

The goal is to build algorithms that bring centimeter-level localization accuracy to smartphones using GNSS measurements and sensor fusion techniques.

🌐 Overview
Traditional smartphone GPS positioning often suffers from poor accuracy—especially in dense urban environments, where buildings interfere with satellite signals. 
This challenge pushes the boundaries of what's possible by giving access to raw GNSS and inertial measurement data, allowing participants to apply advanced filtering, 
signal correction, and AI-based estimation techniques.

The challenge spans the 2023–2024 season and includes updates in dataset quality, new sensor metadata, and extended routes in both urban and suburban settings.

🎯 Challenge Objective
Participants must predict accurate positions (latitude, longitude, altitude) of smartphones based on:

Raw GNSS measurements (pseudorange, carrier phase, doppler, etc.)

Sensor data (accelerometer, gyroscope)

Ground truth positions from high-precision RTK (Real-Time Kinematic) receivers

The competition metric is mean position error (in meters) compared to ground truth across all time points.

🗃️ Dataset
Devices: Google Pixel 4, 5, 6 Pro, etc.

Sensors: GNSS + IMU (Accelerometer, Gyroscope)

Locations: Urban canyons, suburban roads, open highways

Format: CSV, RINEX, NMEA, and derived data formats

Labels: High-accuracy positioning using RTK as ground truth

Note: Data is anonymized, synchronized, and partitioned into training, public test, and private test sets.

🧠 Key Features
📊 Exploratory Data Analysis (EDA) for signal quality, satellite geometry, and positional noise

🛰️ GNSS Preprocessing: Pseudorange correction, satellite bias handling, clock drift adjustments

🔁 Sensor Fusion: Kalman filters, complementary filters, and deep learning-based fusion

📈 Modeling: Classical statistical methods and advanced ML techniques for trajectory estimation

🌐 Map Matching (optional): Use of road maps and prior knowledge to constrain predictions

🛠️ Tools & Technologies
Python 3.x

pandas, numpy, scipy

scikit-learn, XGBoost, LightGBM

TensorFlow / PyTorch (for deep learning models)

FilterPy for Kalman Filtering

Plotly, Seaborn, Matplotlib for visualizations

Pyproj, Geopy for coordinate transformation

Jupyter Notebooks and Colab for experimentation

📈 Evaluation Metric
The primary evaluation metric is Mean 3D Position Error between predicted and ground truth positions across all evaluation sets.

🧪 Use Cases
Improving navigation in urban environments

Enhancing safety in autonomous vehicles and drones

Powering location-based AR applications

Advancing GNSS signal research and corrections

🔮 Future Plans
Expand support for RTKLIB-based solutions

Add real-time streaming inference from mobile device logs

Benchmark deep learning models vs traditional filtering

Create a live demo web interface for path visualization
