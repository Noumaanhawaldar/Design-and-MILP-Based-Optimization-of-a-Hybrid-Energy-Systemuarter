# Optimization of a Smart Energy Hub System using MILP in Python

This project involved the design and techno-economic analysis of a municipal energy supply system with thermoelectric coupling. The core of the project is a **Mixed-Integer Linear Programming (MILP)** model built in Python to optimize energy distribution, resulting in **15% cost savings**.

Key Features:
- Component Integration: Models PV systems, heat pumps, gas boilers, thermal storage, battery storage, and grid connections.
- Multi-Objective Optimization: Finds Pareto-optimal solutions balancing economic costs and carbon emissions.
- Regulatory Compliance: Enforces German legislation limiting fossil fuel heat share to ≤35%.
- Technical Constraints: Implements minimum runtime/downtime requirements for heat pumps.
- Realistic Data: Uses actual meteorological data and load profiles for accurate simulation.

System Components:
- PV System |	356 kWp |	Primary electricity generation
- Heat Pump |	169.5 kW thermal output (COP=3) |	Main heating source
- Gas Boiler | 240 kW thermal output (η=91%) | Backup/peak heating
- Thermal Storage |	1000 kWh capacity |	Heat shifting and storage
- Battery Storage |	48 kWh capacity	Electricity storage
- Grid Connection |	Electricity import/export |	Balance supply and demand

Key Results:
The model calculates:
- Yearly CAPEX and OPEX for the energy system.
- Levelized Cost of Energy (LCOE) for delivered thermal energy.
- CO₂ emissions for different system configurations.
- Hourly operation schedule for all components.
- Pareto frontier comparing cost-optimized vs. CO₂-optimized configurations.

Technical Implementation:
- Framework: Oemof (Open Energy Modeling Framework)
- Optimization: Mixed-Integer Linear Programming (MILP)
- Solver: CBC (Coin-or branch and cut)
- Constraints: Minimum uptime/downtime for heat pumps (6h/2h) | Storage minimum charge levels (20%) | Maximum fossil fuel share (35% of heat production)

Conclusion:
- For the selection of a better model in terms of CO2 emission factor, it is recommended to use the model having CHP and Heat Pump. There is a significant reduction in the consumption of electricity from the Private grid. 
- The excess electricity from CHP and PV is being fed into the grid, which generates revenue.

Author: 
- Noumaan Hawaldar
- Master's Student in International Energy Engineering
- Email: hawaldarnoumaan04@gmail.com
- LinkedIn: linkedin.com/in/noumaan-hawaldar
- This project was developed as part of my Master's studies at Ostbayerische Technische Hochschule Amberg-Weiden, focusing on sustainable energy system design and optimization.
