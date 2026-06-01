<p align="center">
  <h1 align="center">Camera-Less In-Seat Posture Classification<br>& Pose Reconstruction Using Pressure Sensor Fusion</h1>
</p>

<p align="center">
  <strong>Privacy-Preserving In-Cabin Occupant Monitoring System</strong><br>
  International Institute of Information Technology, Bangalore (IIIT-B)
</p>

<p align="center">
  <img src="https://img.shields.io/badge/AI-Two--Stream_CNN-blue?style=flat-square" alt="AI">
  <img src="https://img.shields.io/badge/Reconstruction-LightGBM-critical?style=flat-square" alt="LightGBM">
  <img src="https://img.shields.io/badge/Application-Driver_Monitoring-informational?style=flat-square" alt="Application">
  <img src="https://img.shields.io/badge/Privacy-Camera--Less-brightgreen?style=flat-square" alt="Privacy">
</p>

---

## Table of Contents

* [Overview](#overview)
* [Motivation](#motivation)
* [Key Features](#key-features)
* [System Architecture](#system-architecture)
* [Hardware Setup](#hardware-setup)
* [AI Models](#ai-models)
* [Dataset](#dataset)
* [Technical Highlights](#technical-highlights)
* [Applications](#applications)
* [Repository Structure](#repository-structure)
* [Authors](#authors)
* [License](#license)

---

## Overview

This project presents a privacy-preserving in-cabin monitoring system that performs real-time posture classification and camera-less 2D pose reconstruction using pressure sensor fusion.

Unlike conventional vision-based driver monitoring systems, this framework relies entirely on:

* Pressure sensors
* mmWave radar
* Infrared proximity sensors

to monitor occupant posture and behavior without capturing visual data.

The system accurately classifies:

* Good posture
* Bad posture
* Drowsy posture

while simultaneously reconstructing a real-time 2D stick-figure representation of the occupant.

---

## Motivation

Modern driver monitoring systems often rely on cameras, raising concerns regarding:

* User privacy
* Data storage
* Lighting sensitivity
* Occlusion handling

This project explores a completely non-visual sensing approach for intelligent transportation systems using low-cost pressure and proximity sensors.

The proposed framework enables:

* Privacy-preserving monitoring
* Real-time posture analysis
* Lightweight edge-AI deployment
* Robust operation under all lighting conditions

---

## Key Features

| Feature                              | Description                                 |
| :----------------------------------- | :------------------------------------------ |
| **99.8% Posture Accuracy**           | Two-Stream CNN-based posture classification |
| **98% Pose Reconstruction Accuracy** | Real-time 2D pose estimation                |
| **Camera-Less Operation**            | Fully privacy-preserving framework          |
| **Pressure Sensor Fusion**           | Combines grid and discrete pressure sensors |
| **Real-Time Visualization**          | Smooth live pose reconstruction             |
| **Lightweight AI Models**            | Suitable for embedded deployment            |

---

## System Architecture

The system integrates multiple sensing modalities for occupant monitoring.

### Sensor Components

| Sensor                       | Function                      |
| :--------------------------- | :---------------------------- |
| 15×15 Velostat Pressure Grid | Seat pressure mapping         |
| 8 Discrete Pressure Sensors  | Seatback and seatbelt sensing |
| 60 GHz mmWave Radar          | Heart-rate monitoring         |
| IR Proximity Sensors         | Head movement detection       |

### Processing Pipeline

1. Sensor data acquisition
2. Pressure map preprocessing
3. CNN-based posture classification
4. LightGBM-based pose reconstruction
5. Real-time visualization

---

## Hardware Setup

### Pressure Sensors

* 1× 15×15 Velostat pressure grid
* 8× discrete Velostat pressure sensors

### Physiological Sensor

* 1× 60 GHz mmWave radar module

### Head Tracking

* 2× IR proximity sensors

### Processing Unit

* Arduino / ESP32 based sensor aggregation

---

## AI Models

### Posture Classification

* Two-Stream CNN architecture
* Multi-input pressure fusion
* Real-time inference pipeline

### Pose Reconstruction

* LightGBM regression-based reconstruction
* 2D stick-figure pose generation
* Data smoothing and temporal filtering

---

## Dataset

The datasets used for training and evaluation are available below:

### Posture Dataset

```text
https://drive.google.com/file/d/1JLw3KQFovhRVHnSLNMCSxtxn_WFhPN7F/view
```

### Reconstruction Dataset

```text
https://drive.google.com/file/d/1sSIDQ1Y8VU3BiB1XTWVjd20lRIDnXDxG/view
```

---

## Technical Highlights

| Metric                          | Result      |
| :------------------------------ | :---------- |
| Posture Classification Accuracy | 99.8%       |
| Pose Reconstruction Accuracy    | 98%         |
| Reconstruction Sensors Used     | 8           |
| Monitoring Type                 | Camera-Less |
| Real-Time Capability            | Yes         |

---

## Applications

* Driver Monitoring Systems (DMS)
* Occupant Safety Monitoring
* Smart Vehicles
* Intelligent Transportation Systems
* Edge AI Healthcare Monitoring
* Privacy-Preserving Human Sensing

---

## Repository Structure

```text
.
├── Dataset/
├── Posture_Classification/
├── Pose_Reconstruction/
├── Sensor_Fusion/
├── Hardware/
├── Visualization/
├── Models/
├── Results/
├── Documentation/
└── README.md
```

---

## Authors

| Name           | Affiliation    |
| :------------- | :------------- |
| Siddhant Deore | IIIT Bangalore |
| Hrushikesh Sawant | IIIT Bangalore |
| Madhav Rao | IIIT Bangalore |


---

## License

This project is intended for academic and research purposes.

---

<p align="center">
  <sub>© 2026 · IIIT Bangalore · Intelligent Transportation Research Project</sub>
</p>
