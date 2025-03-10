# 🏙️ Real-Time Smart City Data Streaming and Analytics Pipeline 🚀

Welcome to the **Real-Time Smart City Data Streaming and Analytics Pipeline** project! This project demonstrates how to build a real-time data processing pipeline for smart city data using **Apache Spark**, **Kafka**, and **AWS S3**. The pipeline simulates, processes, and analyzes data streams from vehicles, GPS, traffic cameras, weather sensors, and emergency incidents.

---

## 📋 Table of Contents
1. [Project Overview](#-project-overview)
2. [Technologies Used](#-technologies-used)
3. [Project Architecture](#-project-architecture)
4. [How It Works](#-how-it-works)
5. [Flowchart](#-flowchart)
6. [Getting Started](#-getting-started)
7. [Contributing](#-contributing)
8. [License](#-license)

---

## 🚀 Project Overview

This project simulates real-time smart city data streams, processes them using **Apache Spark Streaming**, and stores the processed data in **AWS S3** for analytics. The pipeline is containerized using **Docker** for easy deployment and scalability.

### Key Features:
- **Real-Time Data Simulation**: Simulate data streams for vehicles, GPS, traffic, weather, and emergencies.
- **Stream Processing**: Process and analyze data in real-time using **Spark Streaming**.
- **Data Storage**: Store processed data in **AWS S3** in Parquet format for efficient querying.
- **Scalable and Containerized**: Deploy the pipeline using **Docker** and **Docker Compose**.

---

## 🛠️ Technologies Used

### Programming Languages
- **Python** 🐍
- **SQL** 📊

### Big Data Tools
- **Apache Spark** 🔥
- **Apache Kafka** 📡
- **Apache Hadoop** 🐘

### Cloud Technologies
- **AWS S3** ☁️
- **AWS IAM** 🔑

### Containerization
- **Docker** 🐳
- **Docker Compose** 🛠️

### Data Formats
- **JSON** 📄
- **Parquet** 🗂️

---

## 🏗️ Project Architecture

The project architecture consists of the following components:

1. **Data Simulation**: A Python script generates simulated smart city data.
2. **Kafka Producer**: Publishes the simulated data to Kafka topics.
3. **Kafka Topics**: Stores the data streams (e.g., `vehicle_data`, `gps_data`).
4. **Spark Streaming**: Consumes and processes the data streams in real-time.
5. **AWS S3**: Stores the processed data in Parquet format.
6. **Data Analytics**: Query and visualize the stored data using tools like AWS Athena or Tableau.

---

## 🎯 How It Works

1. **Data Simulation**:
   - A Python script simulates real-time data for vehicles, GPS, traffic, weather, and emergencies.
   - Example: Vehicle data includes `id`, `deviceId`, `timestamp`, `location`, `speed`, etc.

2. **Kafka Producer**:
   - The simulated data is published to Kafka topics using a Kafka producer.

3. **Kafka Topics**:
   - Kafka topics store the incoming data streams until they are consumed by the Spark Streaming application.

4. **Spark Streaming**:
   - The Spark Streaming application consumes data from Kafka topics.
   - It processes the data (e.g., filtering, aggregating, transforming) and writes it to AWS S3.

5. **AWS S3**:
   - Processed data is stored in Parquet format for efficient querying and analytics.

6. **Data Analytics**:
   - The stored data is queried and visualized using tools like AWS Athena, Tableau, or Power BI.

---

## 📊 Flowchart

```plaintext
+-------------------+       +-------------------+       +-------------------+
|                   |       |                   |       |                   |
|  Data Simulation  |       |  Kafka Producer   |       |  Kafka Topics     |
|  (Python Script)  +------>+  (Python Script)  +------>+  (Vehicle, GPS,   |
|                   |       |                   |       |  Traffic, Weather,|
+-------------------+       +-------------------+       |  Emergency)       |
                                                        +---------+---------+
                                                                  |
                                                                  |
                                                                  v
                                                        +---------+---------+
                                                        |                   |
                                                        |  Kafka Consumer   |
                                                        |  (Spark Streaming)|
                                                        |                   |
                                                        +---------+---------+
                                                                  |
                                                                  |
                                                                  v
                                                        +---------+---------+
                                                        |                   |
                                                        |  Data Processing  |
                                                        |  (Spark Streaming)|
                                                        |                   |
                                                        +---------+---------+
                                                                  |
                                                                  |
                                                                  v
                                                        +---------+---------+
                                                        |                   |
                                                        |  Data Storage     |
                                                        |  (AWS S3 - Parquet|
                                                        |  Format)          |
                                                        |                   |
                                                        +---------+---------+
                                                                  |
                                                                  |
                                                                  v
                                                        +---------+---------+
                                                        |                   |
                                                        |  Data Analytics   |
                                                        |  (Querying &      |
                                                        |  Visualization)   |
                                                        |                   |
                                                        +-------------------+
