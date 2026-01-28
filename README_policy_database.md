# US Composting Policy Database & Geospatial Analysis

**Author:** Sydney Seiter 
**Date:** January 2026  
**Context:** Prepared for COMPOST2026 Conference

## Project Overview

This project develops a comprehensive database of composting regulations, organics bans, and policy incentives across all 50 US states and major municipalities. Building on work conducted for the U.S. Composting Council, this analysis identifies policy trends, geographic clusters, and correlations between regulatory frameworks and composting infrastructure development.

## Business Impact

- **For Policymakers:** Evidence-based insights on effective organics diversion strategies
- **For Facility Operators:** Navigation tool for multi-state regulatory compliance
- **For Industry Advocates:** Data-driven arguments for policy expansion
- **Market Intelligence:** Identifying high-growth regions for composting infrastructure investment

## Key Features

1. **Automated Policy Database**: Structured data on composting regulations from 50 states + DC
2. **Geospatial Analysis**: Heat maps showing policy intensity and infrastructure gaps
3. **Temporal Trends**: Timeline of organics ban adoption and policy evolution
4. **Correlation Analysis**: Relationships between policy types and diversion rates
5. **Predictive Modeling**: Identifying states likely to adopt new policies

## Technical Stack

- **Python 3.9+**
- **Pandas** - Data manipulation and analysis
- **GeoPandas** - Geospatial operations
- **SQLite** - Database management
- **Matplotlib/Seaborn** - Visualization
- **Folium** - Interactive mapping
- **Scikit-learn** - Predictive modeling

## Data Sources

- U.S. Composting Council state regulations database
- ReFED U.S. Food Waste Policy Finder
- Institute for Local Self-Reliance Compost Policy Hub
- State environmental agency websites (EPA, CalRecycle, etc.)
- BioCycle magazine policy coverage

## Key Findings (Example Dataset)

**Methodology Note:** This analysis demonstrates the framework using synthetic policy data structured to match real-world patterns. Numbers shown are illustrative examples of what the analysis would reveal with actual policy databases.

When implemented with real data from USCC, ReFED, and state agencies, this framework can identify:
- **Actual policy adoption patterns** across states and regions
- **Real correlations** between policy types and infrastructure development
- **Genuine high-opportunity markets** for facility expansion
- **Evidence-based insights** for advocacy and policy design

**Example findings from demonstration:**

- **23 states** have commercial organics bans or mandates
- **15 states** have compost procurement requirements for state agencies
- **Strong correlation** (r=0.72) between policy stringency and per-capita composting infrastructure
- **West Coast + Northeast** lead in policy adoption; **Southeast** shows emerging growth
- States with **EPR programs** show 2.3x faster infrastructure development

## Repository Structure

```
project1-policy-database/
├── README.md                          # This file
├── composting_policy_analysis.ipynb   # Main Jupyter notebook
├── data/
│   ├── state_policies.csv            # Policy database (synthetic example)
│   ├── us_states.geojson             # State boundary geometries
│   └── facility_locations.csv         # Composting facility coordinates
├── outputs/
│   ├── policy_heatmap.html           # Interactive map
│   ├── policy_trends.png             # Temporal analysis
│   └── correlation_matrix.png         # Policy-infrastructure relationships
└── requirements.txt                   # Python dependencies
```

## Installation & Usage

```bash
# Clone repository
git clone https://github.com/Buffy686/composting-policy-database.git
cd composting-policy-database

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run Jupyter notebook
jupyter notebook composting_policy_analysis.ipynb
```

## Future Enhancements

- [ ] Real-time web scraping of state legislation databases
- [ ] Natural language processing of policy text for automated classification
- [ ] Integration with USCC facility database for infrastructure analysis
- [ ] API development for policy lookup by location
- [ ] Predictive model for state-level policy adoption timing

## Applications at COMPOST2026

This analysis framework can help:
- **Facility developers** identify underserved markets with strong policy support
- **Industry associations** prioritize advocacy efforts in high-potential states
- **Researchers** quantify policy effectiveness on organics diversion
- **Consultants** provide data-driven regulatory guidance to clients

## Contact & Collaboration

Interested in collaborating on composting policy analysis? Let's connect at COMPOST2026 or reach out via sydney.seiter22@gmail.com.

---

**License:** MIT  
**Citation:** If you use this analysis framework, please cite: Sydney Seiter. (2026). US Composting Policy Database & Geospatial Analysis. GitHub repository.
