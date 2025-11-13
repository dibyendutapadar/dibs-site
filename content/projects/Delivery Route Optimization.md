---
title: Delivery Route Optimization
summary: Optimizes last-mile delivery routes using OR-Tools and Streamlit.
tags: ["Route Optimization", "OR-Tools", "Logistics", "Python"]
categories: ["Projects", "Optimization"]
draft: false
weight: 8
cover:
  image: "/img/20251113214025.png"    
  alt: "Delivery Route Optimization"
---

This application simulates the planning of delivery routes for a specified number of locations and delivery agents within Bangalore. The algorithm used is the Vehicle Routing Problem (VRP) solver provided by [OR-Tools](https://developers.google.com/optimization), an optimization library developed by Google.

### Algorithm
The Vehicle Routing Problem (VRP) is a combinatorial optimization and integer programming problem that seeks to service a number of customers with a fleet of vehicles. It is a generalization of the Traveling Salesman Problem (TSP).

- **Step 1:** Generate a warehouse location and random delivery locations within Bangalore.
- **Step 2:** Use OR-Tools to solve the VRP with the specified number of delivery agents to minimize the total distance traveled.
- **Step 3:** Display the routes for each delivery agent on the map and show the total distance traveled.

The algorithm ensures that the delivery routes are optimized for minimal travel distance, taking into account the constraints of the VRP.

**Key Features**
- Uses Google OR-Tools for path optimization  
- Balances workloads and reduces total delivery time  
- Generates interactive route visualizations  

**Technologies Used**: OR-Tools, Python, Streamlit  

🔗 [GitHub](https://github.com/dibyendutapadar/delivery-routing-optimization)  
📱 [App Link](https://delivery-routing-optimization.streamlit.app/)
