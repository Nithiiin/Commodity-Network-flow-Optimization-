# Edge Disjoint Minimum Cost Multicommodity Flow Network

## Project Overview

This project addresses the **Edge-Disjoint Minimum Cost Multicommodity Flow Problem (MCNF)** using optimization techniques. The objective is to minimize costs while ensuring edge-disjoint paths for commodities in a given graph network. The problem is solved with linear programming and tested using real-world road networks.


---

## Problem Statement

Given a directed graph \( G(V, E) \), where:
- \( V \) represents nodes
- \( E \) represents edges
- Multiple commodities \( k \) need to be transported between supplier (origin) and terminal (destination) nodes.

The main objectives are:
1. **Minimize the total transportation cost**.
2. Ensure the **edge disjoint constraint** (each edge can only be traversed once).

---

## Methodology

- The problem is formulated as a **linear programming model**.
- Edge capacities are set to **1** to enforce edge-disjoint flows.
- The optimization is performed using the **Gurobi Optimizer**.
- Graph data is handled using the **NetworkX** library in Python.
- Road network data is tested for **single commodity**, **2 commodities**, **3 commodities**, and **4 commodities**.

---
## Commodities Overview

### 1. Single Commodity Flow
- **Description**:  
  Solves the minimum cost flow for one origin-destination pair.
- **File**: `SINGLE_COMMODITY.ipynb`
- **Output**:  
  A single optimal path with minimum cost.

---

### 2. Two Commodities Flow
- **Description**:  
  Solves for two commodities with two origins and two destinations while ensuring edge-disjoint paths.
- **File**: `2_COMMODITIES.ipynb`
- **Output**:  
  Edge-disjoint paths are successfully computed for both commodities.  
  - **Origin Nodes**: 2  
  - **Destination Nodes**: 2  
  - **Edge Constraint**: Each edge can only be traversed once.

---

### 3. Three Commodities Flow
- **Description**:  
  Solves for three commodities with three origins and three destinations.
- **File**: `3_COMMODITIES.ipynb`
- **Output**:  
  Edge-disjoint paths are computed successfully for all three commodities.  
  - **Origin Nodes**: 3  
  - **Destination Nodes**: 3  
  - **Edge Constraint**: Edge capacity = 1.

---

### 4. Four Commodities Flow
- **Description**:  
  Attempts to solve for four commodities with four origins and four destinations.  
  - Results in **infeasibility** due to edge constraints (no disjoint paths available).
- **File**: `4_COMMODITIES.ipynb`
- **Output**:  
  - **Feasibility**: Infeasible solution.  
  - Network cannot handle more than 3 commodities while ensuring edge disjoint flows.



