# 🚗 Model_2 (CapstoneProject) – Dynamic Pricing for Urban Parking Lots

This repository contains the implementation of **Model 2: Demand-Based Pricing** as part of the Summer Analytics 2025 Capstone Project hosted by **Consulting & Analytics Club × Pathway**.

The goal is to design a **real-time pricing engine** for urban parking spaces based on demand, environmental conditions, and vehicle data.

---

## 🧠 Project Overview

Urban parking is a limited and high-demand resource. Static pricing leads to inefficiencies—either overutilization or underutilization. This project builds a **dynamic pricing model** that adjusts in real time using:

- Occupancy rates
- Traffic congestion
- Queue length
- Vehicle type
- Special event indicators

---

## 🛠 Tech Stack

- **Python**
- **Jupyter Notebook**
- **Pandas, NumPy**
- **Pathway** (for real-time simulation)
- **Bokeh** (for live visualization)
- **Panel** (dashboard support)

---

## 🏗️ Architecture Diagram

```mermaid
flowchart TD
    A[Raw CSV Dataset (14 lots × 73 days)] --> B[Pathway Streaming Engine]
    B --> C[Real-time Data Preprocessing]
    C --> D[Demand Function Calculator]
    D --> E[Dynamic Price Calculator]
    E --> F[Bokeh Real-Time Visualization]
    E --> G[Optional: Rerouting Suggestions]
```

---

## 🔄 Project Workflow

1. **Data Simulation:**
   - The dataset contains records for 14 parking lots, each with features like occupancy, queue, vehicle type, traffic, etc.
   - Simulated via Pathway to mimic real-time streaming.

2. **Demand Function:**
   - Constructed using weighted linear components:
     - `Occupancy / Capacity`
     - `Queue Length`
     - `Traffic Level`
     - `Is Special Day`
     - `Vehicle Type Weight`
   - Demand is normalized.

3. **Dynamic Pricing:**
   - Starts from a base price of $10.
   - New Price = `BasePrice × (1 + λ × NormalizedDemand)`
   - Smooth variation ensured by bounding price between 0.5× and 2× base.

4. **Visualization:**
   - Real-time graphs built using **Bokeh** to monitor price trends for each lot.

5. **Extensions:**
   - Competitor pricing and rerouting strategies can be added (Model 3).

---

## 📁 File Structure

```bash
.
├── Model_2xx.ipynb            # Main notebook with pricing logic
├── dataset.csv                # Cleaned and structured input data
├── problem statement.pdf      # Detailed task & expectations
├── README.md                  # Project summary and documentation
```

---

## 📊 Output Examples

- Real-time line plots showing price evolution
- Responsive to traffic levels, queue length, and occupancy
- Modular structure allows plugging in Model 3 logic

---

## 📌 Key Notes

- Only **pandas**, **numpy**, and **Pathway** were used (per project constraint).
- Implemented pricing model is smooth, interpretable, and modular.
- Can scale to multiple parking spots and integrate competitive pricing logic.

---

## 📄 Optional Report

If available, a PDF report explaining the model in depth (assumptions, demand weights, etc.) can be added here.

---

## 📬 Contact

For queries or collaboration, feel free to reach out to the project contributor.

---
