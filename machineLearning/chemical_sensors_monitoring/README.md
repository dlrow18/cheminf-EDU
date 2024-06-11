# Sensor Data Analysis

## Overview

This repository contains a dataset collected from a sensor over a period of time. The dataset includes information about sensor readings, temperature, humidity, and degradation levels recorded at different timestamps.

## Dataset Description

The dataset consists of the following fields:

- **SensorID**: Identifier for the sensor.
- **Timestamp**: The date and time when the data was recorded.
- **SensorValue**: The value recorded by the sensor.
- **Temperature**: The temperature at the time of recording.
- **Humidity**: The humidity level at the time of recording.
- **DegradationLevel**: The level of degradation recorded at the time of recording.

## Sample Data

## Usage

This dataset can be used for various types of analysis including but not limited to:

- Time series analysis to track changes in sensor values, temperature, humidity, and degradation levels over time.
- Distribution analysis to understand the frequency and spread of different recorded values.
- Correlation analysis to explore relationships between different variables in the dataset.
- Anomaly detection to identify unusual patterns or values.

## Visualization

Here are some suggested visualizations to gain insights from the dataset:

1. **Line Charts**: To visualize trends over time for `SensorValue`, `Temperature`, `Humidity`, and `DegradationLevel`.

    ```python
    plt.figure(figsize=(12, 6))
    plt.plot(df['Timestamp'], df['SensorValue'], label='SensorValue')
    plt.plot(df['Timestamp'], df['Temperature'], label='Temperature')
    plt.plot(df['Timestamp'], df['Humidity'], label='Humidity')
    plt.plot(df['Timestamp'], df['DegradationLevel'], label='DegradationLevel')
    plt.legend()
    plt.title('Time Series Data')
    plt.xlabel('Timestamp')
    plt.ylabel('Values')
    plt.show()
    ```

2. **Histograms**: To show the distribution of `SensorValue`, `Temperature`, `Humidity`, and `DegradationLevel`.

    ```python
    df.hist(figsize=(10, 8))
    plt.suptitle('Histograms of Sensor Data')
    plt.show()
    ```

3. **Scatter Plots**: To explore relationships between different variables.

    ```python
    sns.pairplot(df[['SensorValue', 'Temperature', 'Humidity', 'DegradationLevel']])
    plt.suptitle('Scatter Plot Matrix')
    plt.show()
    ```

4. **Box Plots**: To visualize the distribution and identify any outliers.

    ```python
    plt.figure(figsize=(12, 6))
    sns.boxplot(data=df[['SensorValue', 'Temperature', 'Humidity', 'DegradationLevel']])
    plt.title('Box Plots of Sensor Data')
    plt.show()
    ```

5. **Heatmap**: To show correlations between all pairs of variables.

    ```python
    plt.figure(figsize=(10, 8))
    sns.heatmap(df[['SensorValue', 'Temperature', 'Humidity', 'DegradationLevel']].corr(), annot=True, cmap='coolwarm')
    plt.title('Correlation Heatmap')
    plt.show()
    ```

## Dependencies

To run the code snippets provided in this README, you need the following Python packages:

- pandas
- matplotlib
- seaborn
- datetime

You can install these packages using pip:

```sh
pip install pandas matplotlib seaborn

