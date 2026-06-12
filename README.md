# 🌡️ IoT Real-Time Temperature & Humidity Monitoring Dashboard

An end-to-end IoT monitoring system that collects real-time temperature and humidity data using an ESP32 microcontroller and DHT11 sensor. Sensor readings are transmitted via MQTT (with HTTP fallback support), processed by a Node.js backend, stored in an SQLite database, and visualized through a responsive React dashboard with live updates.

## 🚀 Overview

This project demonstrates a complete IoT pipeline:

* 📡 Data acquisition using ESP32 + DHT11
* 🔄 MQTT-based communication with HTTP fallback
* 🗄️ Persistent storage using SQLite
* ⚡ Real-time streaming using Server-Sent Events (SSE)
* 📊 Interactive dashboard built with React and Recharts
* 📈 Historical analysis and environmental statistics

## 🏗️ System Architecture

```text
DHT11 Sensor
      │
      ▼
ESP32 Microcontroller
      │
      ├── MQTT (HiveMQ Broker)
      └── HTTP Fallback
      │
      ▼
Node.js + Express Backend
      │
      ├── SQLite Database
      └── SSE Streaming
      │
      ▼
React Dashboard
```

## 🛠️ Tech Stack

### Hardware

* ESP32 Development Board
* DHT11 Temperature & Humidity Sensor

### Backend

* Node.js
* Express.js
* MQTT (PubSubClient / HiveMQ Broker)
* SQLite (better-sqlite3)
* Server-Sent Events (SSE)

### Frontend

* React.js
* Vite
* Tailwind CSS
* Recharts

## ✨ Features

### Real-Time Monitoring

* Live temperature updates
* Live humidity tracking
* Automatic dashboard refresh via SSE

### Data Management

* SQLite-based persistent storage
* Historical data retrieval
* Data migration support

### Analytics

* Minimum, maximum, and average calculations
* Historical trend visualization
* Environmental comfort indicators

### Connectivity

* MQTT communication
* HTTP fallback endpoint
* Reliable sensor-to-dashboard pipeline

## 📡 API Endpoints

| Method | Endpoint              | Description                      |
| ------ | --------------------- | -------------------------------- |
| GET    | `/api/sensor/latest`  | Get latest sensor reading        |
| GET    | `/api/sensor/history` | Retrieve historical readings     |
| GET    | `/api/sensor/stats`   | Get min, max, and average values |
| GET    | `/api/sensor/stream`  | Real-time SSE stream             |
| POST   | `/api/sensor/data`    | Submit sensor data               |
| DELETE | `/api/sensor/data`    | Clear stored data                |

## 🔧 Hardware Connections

| DHT11 | ESP32  |
| ----- | ------ |
| VCC   | 3.3V   |
| DATA  | GPIO 4 |
| GND   | GND    |

## 📊 Dashboard Highlights

* Real-time temperature visualization
* Humidity trend monitoring
* Interactive charts
* Statistical summaries
* Responsive UI design

## 🎯 Learning Outcomes

This project demonstrates practical implementation of:

* Internet of Things (IoT) systems
* MQTT messaging protocol
* Real-time web applications
* RESTful API development
* Database integration
* ESP32 programming
* React dashboard development

## 📸 Preview

Add screenshots of your dashboard here.

## 👨‍💻 Author

Developed as part of an Industry-Oriented R&D Internship at Precision Informatics.

### Project Goal

To build a scalable and real-time IoT monitoring solution capable of collecting, storing, analyzing, and visualizing environmental sensor data using modern web technologies and embedded systems.
