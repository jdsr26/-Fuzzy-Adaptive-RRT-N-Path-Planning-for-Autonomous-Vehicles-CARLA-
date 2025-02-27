# -Fuzzy-Adaptive-RRT-N-Path-Planning-for-Autonomous-Vehicles-CARLA-
Implements FA-RRTN, a fuzzy logic-enhanced RRT variant, to optimize path planning in dynamic environments. Integrates with CARLA for simulation, achieving 84% faster computation, 68% fewer nodes, and shorter paths (6.57m vs. 7.01m) vs. RRT*. Built in Python with CARLA, NumPy, and fuzzy logic.
# FA-RRT*N Path Planning for Autonomous Vehicles in CARLA  
[![Python 3.8+](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![CARLA 0.9.14](https://img.shields.io/badge/CARLA-0.9.14-green)](https://carla.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-orange)](LICENSE)

<img src="assets/RRT_vs_FA-RRTN.png" width="700" alt="Performance Comparison">

## Overview  
This repository implements the **Fuzzy Adaptive RRT*N (FA-RRT*N)** algorithm, a high-efficiency path planner for autonomous vehicles. By integrating fuzzy logic with normal distribution-guided node generation, FA-RRT*N achieves **84% faster computation** and **68% fewer nodes** compared to traditional RRT*. Validated in CARLA, a realistic autonomous driving simulator.

## Key Features  
- 🧠 **Fuzzy Logic Adaptation**: Dynamically adjusts node distribution using obstacle density and goal proximity.  
- 🚗 **CARLA Integration**: Simulate paths with a Tesla Model 3 in urban environments.  
- 📊 **Benchmarked Performance**: 25-run comparison with RRT* (time, nodes, path length).  

## Performance  
| Metric          | RRT*       | FA-RRT*N   | Improvement |  
|-----------------|------------|------------|-------------|  
| Time (avg)      | 0.9156s    | **0.146s** | 84% faster  |  
| Nodes (avg)     | 776        | **247**    | 68% fewer   |  
| Path Length     | 7.0124m    | **6.5772m**| 6.2% shorter|  

## Installation  
```bash
git clone https://github.com/yourusername/FA-RRT-starN-CARLA.git
cd FA-RRT-starN-CARLA
pip install -r requirements.txt
```
CARLA Setup
Download CARLA 0.9.14 from the official site.

Extract and run CarlaUE4.sh (Linux) or CarlaUE4.exe (Windows).

Usage
Run FA-RRT*N
```bash
python src/FA-RRT_star_N.py
```
CARLA Simulation


# Start CARLA server
```bash
./CarlaUE4.sh

# Run simulation script
python src/FA-RRT_star_N_CARLA.py
```
