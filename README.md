
# Summer Analytics project- Dynamic pricing fr Urban parking lots


This repository contains the implementation of a dynamic pricing system for urban parking spaces, developed as part of my **Summer Analytics Capstone Project**.

The goal of this project is to simulate a real-world smart pricing engine that adjusts the price of parking spaces in real time based on **occupancy**, **demand**, **traffic**, **vehicle type**, and **competitor pricing**.

---

##  Technologies Used
- **Language**: Python
- **Libraries**: `pandas`, `numpy`, `geopy`, `matplotlib`, `bokeh` (for initial visualizations)

---

## Models Implemented

### Model 1: Baseline Linear Pricing
A simple pricing model where the next price is based on current occupancy:

Price_t+1 = BasePrice + α × (Occupancy / Capacity)
- Price increases linearly with occupancy.
- Acts as a baseline reference model.


###  Model 2: Demand-Based Price Function
A more intelligent model that considers multiple demand-driving features:

**Features used**:
- Occupancy 
- Queue Length
- Traffic Condition Nearby
- Special Day Indicator
- Vehicle Type (car, bike, truck)
-  Capacity
    
    
**Approach**:
- A custom **demand score** is calculated by assigning random yet logical weights to the above features.

Model 3: Competitive Pricing Model (Optional)
This model adds **location intelligence** and simulates **real-world competition** between nearby lots.

**Logic**:
- Compute geographic distance between lots using **latitude & longitude** (`geopy`).
- If a lot is **overburdened** and nearby lots are cheaper → match or lower price.
- If nearby lots are expensive → increase price to just below competitors.

**Assumption**:
- **Radius = 500 meters** : Competitors are considered only if they are within this range.

---

## Visualizations
- The initial data exploration and visualizations are done using Bokeh (from the starter notebook).
- Plots show how pricing adapts with occupancy, time, and competitive conditions.


 # What I Learned
- How to build custom ML logic from scratch using only **NumPy & Pandas**
- Working with **real-time simulation data**
- Handling **geo-spatial intelligence** and **pricing optimization**
- Visual storytelling using **Bokeh** and **matplotlib**

---
## Appendix

Any additional information goes here


## Badges

Add badges from somewhere like: [shields.io](https://shields.io/)

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)
[![AGPL License](https://img.shields.io/badge/license-AGPL-blue.svg)](http://www.gnu.org/licenses/agpl-3.0)

