# Cargo Network Optimization with PuLP

## Overview
This project formulates and solves a linear programming model for a cargo shipping network. The objective is to minimize total shipping cost while routing freight from hub airports through focus cities to downstream demand centers under capacity, demand, and flow-balance constraints.

## Coursework Context
This repository packages work originally completed as part of Western Governors University's (WGU) M.S. in Data Analytics program and reorganizes it into a public portfolio format. Screenshots extracted from the original written submission are preserved in `assets/report-extracts/`.

## Business Problem
How should cargo be routed across a multi-node network so that all destination demand is satisfied at minimum cost without exceeding hub or focus-city capacity?

## Optimization Formulation
### Objective
Minimize total shipping cost across the network.

### Constraints
- hub capacity constraints
- focus-city processing capacity constraints
- demand satisfaction at every center
- flow balance at each focus city
- non-negativity on all shipment variables

## Tools
- Python
- PuLP
- CBC solver

## Results
- solver status: `Optimal`
- all copied verification outputs in the notebook show hub, focus-city, demand, and flow-balance constraints satisfied

## Included Files
- `notebooks/optimization.ipynb`
- `requirements.txt`

## Note
The publish-only staging copy keeps the notebook and leaves the original report documents out of this GitHub set.
