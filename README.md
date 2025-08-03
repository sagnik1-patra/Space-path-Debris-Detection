 Spacepath Debris Detection and Optimal Route Planning
This project leverages real-time aircraft tracking data from the OpenSky Network to:

Detect anomalous aircraft behavior using ML.

Perform real-time flight monitoring.

Recommend safe and optimal air routes, avoiding risky zones.

 Dataset
Filename: aircraft-data_nov_dec.csv

Path: C:\Users\sagni\Downloads\Spacepath Debris Detection\aircraft-data_nov_dec.csv

Features: Altitude, latitude, longitude, velocity, vertical rate, etc.

 Installation
bash
Copy
Edit
pip install pandas scikit-learn joblib requests flask
 Model Training
Algorithm: Isolation Forest

Input features: Altitude, velocity, lat, lon

Outputs:

isolation_forest_model.pkl

scaler.pkl

Anomaly results in anomaly_results.csv
 Real-Time Monitoring
Run this to flag anomalies using OpenSky live API:

bash
Copy
Edit
python real_time_monitor.py
 Optimal Route Suggestion
Suggests a route between two points while:

Avoiding regions with high anomaly density

Visualizing route and anomalies

 Output Screenshot
 Screenshot Path in Repo:
![Output Screenshot](Screenshot%202025-08-03%20174337.png)



 OpenSky API
Live data source: OpenSky REST API

Use /states/all for anonymous requests or /states/own with credentials for extended access.

 Future Additions
Add weather and satellite overlays

Reinforcement learning-based rerouting

Integration with UAV/drones for in-air coordination
