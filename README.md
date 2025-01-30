# Optimizing-Wind-Farm-Layout-for-Maximum-Energy-Production

**Project Overview**

This project aims to maximize energy production in a wind farm by optimizing turbine placement. Using a gradient descent-based optimization approach, we analyze and adjust turbine positions on a wind map to enhance power output while considering wake effects and spatial constraints.

**Problem Statement**

The challenge is to optimize the layout of 30 wind turbines within a 20 km × 20 km wind farm area to maximize AEP. Each turbine has an 80 m rotor diameter, and placement must respect the following constraints:

    1.) Boundary Constraint: All turbines must be within the farm perimeter, maintaining a minimum distance equal to one rotor diameter from the boundary.
    
    2.) Spacing Constraint: A minimum clearance of 400 m between any two turbines must be maintained.

**Data Used**

The project uses a wind speed map stored in CSV format, representing spatial wind speed distribution across the 20 km × 20 km wind farm area. Each cell in the map corresponds to a specific coordinate on the grid, with values indicating wind speed (in m/s) at that location.

**Wake Effect Modeling**

We use Jensen's wake model to account for the wake effect, which is crucial for accurate energy production estimation.

**Results**

    -Initial power output: 273.55 MW
   - Optimized power output: 285.23 MW
   - Improvement: 11.68 MW (4.26% increase)

**Code Implementation**

The implementation includes the following main components:

1.) Reads wind speed data from a CSV file.
2.) Calculates each turbine's power and applies the wake model.
3.) Defines an objective function to maximize energy output while applying penalties for insufficient spacing.
4.) Uses gradient descent to adjust turbine positions.
5.) Displays the optimized layout.
