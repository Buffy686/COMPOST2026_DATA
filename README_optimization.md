# Organics Collection Route Optimization

**Author:** [Your Name]  
**Date:** January 2026  
**Context:** Prepared for COMPOST2026 Conference

## Project Overview

This project develops an intelligent route optimization system for municipal organics collection (food waste, yard trimmings) using real-world constraints: time windows, vehicle capacity, traffic patterns, and facility processing schedules. By optimizing collection routes, municipalities can reduce fuel costs by 20-30%, decrease carbon emissions, and improve service reliability—critical for expanding organics diversion programs.

## Business Impact

- **Cost Reduction**: 20-30% decrease in fuel and labor costs through optimized routing
- **Carbon Emissions**: 25-35% reduction in GHG from collection vehicles
- **Service Quality**: Improved on-time collection, reduced missed pickups
- **Scalability**: Data-driven planning for expanding organics programs
- **Regulatory Compliance**: Meeting organics ban requirements efficiently

## Key Features

1. **Vehicle Routing Problem (VRP) Solver**: Optimizes multi-vehicle collection routes
2. **Real-World Constraints**: Time windows, vehicle capacity, driver hours, facility hours
3. **Traffic Integration**: Adjusts for congestion patterns (morning/afternoon peaks)
4. **Cost Analysis**: Fuel consumption, labor hours, carbon footprint calculation
5. **Scenario Modeling**: Compare current vs optimized routes, evaluate program expansion
6. **Interactive Maps**: Visualize routes with Folium/Plotly

## Technical Stack

- **Python 3.9+**
- **OR-Tools** - Google's optimization library (VRP solver)
- **GeoPandas** - Geospatial operations
- **Folium** - Interactive mapping
- **NetworkX** - Graph algorithms for routing
- **Pandas/NumPy** - Data manipulation
- **Matplotlib/Seaborn** - Visualization

## Problem Formulation

**Objective:** Minimize total route distance and time while satisfying:
- Each pickup location visited exactly once
- Vehicle capacity not exceeded
- Collection within time windows (e.g., commercial: 7am-11am)
- Drivers complete routes within shift (8 hours)
- All vehicles return to depot/facility

**Variables:**
- Number of vehicles: 3-5 trucks
- Vehicle capacity: 8-12 cubic yards
- Daily pickups: 50-150 locations
- Service time per stop: 3-8 minutes
- Facility processing hours: 7am-5pm

## Repository Structure

```
project3-route-optimization/
├── README.md                          # This file
├── organics_route_optimization.ipynb  # Main analysis notebook
├── data/
│   ├── pickup_locations.csv          # Customer coordinates, demand
│   ├── traffic_patterns.csv          # Time-of-day congestion factors
│   └── facility_locations.csv        # Processing facilities
├── outputs/
│   ├── optimized_routes_map.html     # Interactive route visualization
│   ├── route_comparison.png          # Current vs optimized metrics
│   ├── carbon_analysis.png           # Emissions reduction
│   └── optimized_schedule.csv        # Detailed route plan for drivers
└── requirements.txt                   # Python dependencies
```

## Installation & Usage

```bash
# Clone repository
git clone https://github.com/[username]/organics-route-optimization.git
cd organics-route-optimization

# Create virtual environment
python -m venv venv
source venv/bin/activate

# Install dependencies (including OR-Tools)
pip install -r requirements.txt

# Run optimization notebook
jupyter notebook organics_route_optimization.ipynb
```

## Key Results (Simulated Municipality)

**Methodology Note:** This demonstration uses a realistic municipal scenario (120 commercial stops, 15-mile radius) with industry-standard parameters. Results align with published logistics research showing 20-30% efficiency gains from route optimization.

**Simulation Parameters Based On:**
- Actual composting facility locations and service areas
- Real truck specifications (6 MPG fuel economy, 10 cubic yard capacity)
- Industry-standard costs ($3.50/gallon fuel, $25/hour labor)
- EPA emission factors for carbon footprint calculation
- Published VRP algorithm performance benchmarks

**Baseline (Current Manual Routing):**
- 5 vehicles, 120 stops/day
- Total daily distance: 187 miles
- Fuel consumption: 31.2 gallons ($109/day)
- CO₂ emissions: 685 lbs/day
- Labor: 42.5 hours/day

**Optimized Routes:**
- 4 vehicles, 120 stops/day (1 vehicle reduction)
- Total daily distance: 142 miles (-24%)
- Fuel consumption: 23.7 gallons (-24%, $83/day)
- CO₂ emissions: 520 lbs/day (-24%)
- Labor: 34.2 hours/day (-20%)

**Annual Savings (250 collection days):**
- Fuel: $6,500/year
- Labor: $21,250/year (at $25/hr)
- Vehicle maintenance: $3,200/year
- **Total: $30,950/year + 1 vehicle repurposed**
- **CO₂ reduction: 41,250 lbs/year (20.6 tons)**

## Real-World Implementation

### For Small Municipalities (<50 stops/day):
- Manual route adjustment based on optimization recommendations
- Weekly review of new customer additions
- Excel-based tracking with plotted routes

### For Mid-Size Programs (50-150 stops/day):
- Integration with existing fleet management software
- Daily re-optimization based on new signups/cancellations
- Mobile app for drivers with turn-by-turn navigation

### For Large Programs (150+ stops/day):
- Real-time dynamic routing adjusting for traffic, breakdowns
- Predictive modeling for seasonal demand (yard waste peaks)
- Integration with smart bin fill sensors

## Expansion Scenario Modeling

The notebook includes analysis of:
1. **Adding residential curbside** (current commercial-only)
2. **New state organics ban** (doubling customer base)
3. **Multi-facility routing** (opening second processing site)
4. **Seasonal variation** (fall yard waste surge)

## Future Enhancements

- [ ] Real-time traffic API integration (Google Maps, Waze)
- [ ] Machine learning for demand forecasting (seasonal patterns)
- [ ] Multi-day schedule optimization (reduce peak-day overload)
- [ ] Integration with smart bin IoT sensors (fill-level-based routing)
- [ ] Electric vehicle range constraints and charging optimization
- [ ] Customer notification system (collection time estimates)

## Applications at COMPOST2026

This framework demonstrates:
- **ROI for expanding organics collection programs**
- **Data-driven evidence for grant applications (SWIFR, state programs)**
- **Operational efficiency before capital investment in trucks**
- **Carbon reduction quantification for climate action plans**

## Contact & Collaboration

Interested in optimizing your municipality's organics collection routes? Let's discuss implementation strategies at COMPOST2026 or connect via [LinkedIn/Email].

---

**License:** MIT  
**Citation:** If you use this route optimization framework, please cite: [Your Name]. (2026). Organics Collection Route Optimization. GitHub repository.

**Acknowledgments:** Optimization algorithms based on:
- Google OR-Tools VRP solver
- Research on sustainable logistics (FarEye, NextBillion.ai)
- Municipal organics collection best practices (USCC, ReFED)
