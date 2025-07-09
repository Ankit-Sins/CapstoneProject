# 🚗 Model_1 (CapstoneProject) – Baseline Linear Pricing for Urban Parking Lots

This repository contains the implementation of **Model 1: Baseline Linear Model** as part of the Summer Analytics 2025 Capstone Project hosted by **Consulting & Analytics Club × Pathway**.

The goal is to simulate a simple dynamic pricing system for parking spots based only on current occupancy.

---

## 🧠 Project Overview

Urban parking inefficiencies due to static pricing can be mitigated with dynamic models. This baseline model linearly increases parking price as occupancy rises.

This implementation is a starting point for more sophisticated pricing systems (see Model 2 and Model 3).

---

## 🛠 Tech Stack

- **Python**
- **Google Colab + Jupyter Notebook**
- **Pandas, NumPy**
- **Pathway** (for real-time simulation)
- **Bokeh** (for live visualization)
- **Panel**

---

## 🏗️ Architecture Diagram

```mermaid
flowchart TD
    A[Raw CSV Dataset (single parking lot)] --> B[Pathway Streaming Engine]
    B --> C[Real-time Preprocessing]
    C --> D[Occupancy-Based Price Adjustment]
    D --> E[Real-time Bokeh Visualization]
