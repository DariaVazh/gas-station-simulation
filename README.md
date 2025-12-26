# Gas Station Simulation Model

[![Wolfram Mathematica](https://img.shields.io/badge/Wolfram_Mathematica-13%2B-red.svg)](https://www.wolfram.com/mathematica/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A discrete-event simulation model of a **petrol/gas station (AZS)** as a queueing system, implemented in **Wolfram Mathematica**.

The model simulates customer flow, fuel dispensing at pumps (columns), and payment at cash registers, taking into account real-world factors such as tank side (left/right), payment type, additional purchases, and dynamic queue formation.

Developed as a course project in "Computer Mathematics Systems" at SPbGEU (2025).

## Key Features

- **Realistic customer behavior**:
  - Arrival times (configurable or randomly generated)
  - Fuel amount request (20–60 liters)
  - Tank side: left or right
  - Payment type: cash or card
  - Additional purchases in the shop (yes/no)
- **Infrastructure**:
  - Fuel pumps with specified type (left-side or right-side compatible)
  - Uniform dispensing speed (configurable)
  - Multiple cashiers with equal performance
- **Smart assignment logic**:
  - Random suitable pump selection based on tank side
  - Cashier selection using **shortest queue strategy**
- **Comprehensive statistics**:
  - Maximum queue lengths at pumps and cashiers
  - Maximum idle time for pumps and cashiers
  - Number of served / unserved customers
  - Full simulation timeline tracking
- **Interactive GUI**:
  - Predefined load profiles (light/medium/hard: 250/500/1000 customers)
  - Sliders for real-time parameter adjustment
  - Profile saving/loading/deleting
  - Automatic detection and display of the best configuration (minimal max idle time)
  - Separate statistics window with historical runs

## Screenshots

<img width="1018" height="873" alt="image" src="https://github.com/user-attachments/assets/4a13492d-1120-448d-bf9b-89c5eb1be5cc" />
<img width="863" height="222" alt="image" src="https://github.com/user-attachments/assets/2f0ca57e-ce48-449f-bb79-509182c9c976" />
<img width="372" height="283" alt="image" src="https://github.com/user-attachments/assets/6be186a9-ea3a-4dab-8b59-4cd42e48a070" />

## How to Run

1. Open the main notebook file: `GasStationSimulation.nb`
2. Evaluate all cells (Ctrl+A → Shift+Enter)
3. Use the interactive interface to:
   - Select load profile
   - Adjust number of pumps (1–20), right-side pumps, cashiers (1–10), speed, simulation time
   - Generate random customer data
   - Run simulation
   - View results and best configuration

## Technical Details

- Built entirely in **Wolfram Language (Mathematica)**
- Uses dynamic variables, associations, tables, and manipulates for GUI
- Discrete-time simulation with minute-level granularity
- Queue tracking over time for visualization potential
- Inspired by real queueing theory models (reference: Moazzami et al., 2013)

## Future Improvements

- Integration with real arrival data
- Visualization of queue dynamics over time (graphs)
- Multi-fuel type support
- Staff scheduling optimization
- Export results to CSV/PDF

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## References

- Moazzami A. et al. "Simulation, modeling and analysis of a petrol station" (2013)
- Wolfram Language Documentation: https://reference.wolfram.com

---

Feel free to star ⭐, fork, or use as educational material!
