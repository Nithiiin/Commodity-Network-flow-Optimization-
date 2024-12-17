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


