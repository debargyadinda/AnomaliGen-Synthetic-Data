Synthetic Multivariate Time Series with Anomaly Detection

This project demonstrates the creation, processing, and visualization of a synthetic multivariate time series dataset with integrated anomaly detection. The workflow includes generating a large dataset, detecting anomalies using statistical thresholds and machine learning, and visualizing the results with clear anomaly markers.
Features

CSV file link - https://drive.google.com/file/d/1GjV2H0kEDYl_t1ISpYyE6ClGNUMbzHgc/view?usp=sharing

    Synthetic Data Generation
        Simulates hardware metrics such as Cpu_Temperature, Cpu_Usage, Cpu_Load, Memory_Usage, Battery_Level, and Cpu_Power.
        Generates over 8.64M samples for 24 hours at a sampling rate of 100 Hz.

    Anomaly Simulation![plot](https://github.com/user-attachments/assets/6c1c6bd7-294b-4345-88bc-cfc02edb0a9c)

        Injects anomalies based on pre-defined thresholds (e.g., Cpu_Temperature > 90°C).
        Implements machine learning-based anomaly detection using Isolation Forest.

    Data Processing
        Handles large datasets (1 GB+) using chunked processing to optimize memory usage.
        Applies rolling mean smoothing for trend visualization.

    Visualization
        Plots feature trends with blue lines and anomalies marked as red dots.
        Separates plots for each feature to improve clarity.

Requirements

    Python 3.7+
    Libraries: pandas, numpy, matplotlib, scipy, sklearn, datetime

How to Run

    Clone the repository:

git clone https://github.com/debargyadinda/AnomaliGen-Synthetic-Data.git
cd AnomaliGen-Synthetic-Data

Install required libraries:

pip install -r requirements.txt

Run the script:

    python anomalygen_using_syntheticdata.py

File Structure

    anomalygen_using_syntheticdata.py: Main script for data generation, anomaly detection, and visualization.
    hardware_monitor_data_with_anomalies_large.csv: Generated dataset (created after running the script).

Notes

    The script is executed and tested on Linux for optimal performance with large datasets.
    Anomalies are marked using both statistical thresholds and machine learning models for a robust approach.

Output

The final output includes:

    CSV file containing the generated dataset with anomaly labels.
    Visual plots showing trends for each feature, with anomalies marked as distinct red dots.

License

This project is licensed under the MIT License.
