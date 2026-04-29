# Cargo Network Optimization with PuLP

## Overview
This project formulates and solves a linear programming model for a cargo shipping network. The objective is to minimize total shipping cost while routing freight from hub airports through focus cities to downstream demand centers under capacity, demand, and flow-balance constraints.

## Academic Context
Completed during my M.S. in Data Analytics at Western Governors University (WGU), then packaged here as a reproducible public portfolio project. Screenshots from the original written submission are preserved in `assets/report-extracts/`.

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
- total minimum cost: `$200,863.75`
- solver status: `Optimal`
- CVG was fully utilized at `95,650` tons, while AFW carried `38,097` of `44,350` available tons
- all saved verification outputs in the notebook show hub, focus-city, demand, and flow-balance constraints satisfied

## Included Files
- `notebooks/optimization.ipynb`
- `requirements.txt`

## Selected Visuals

![Optimization report visual 1](assets/report-extracts/report_image_01.png)

![Optimization report visual 2](assets/report-extracts/report_image_02.png)

## Note
The notebook contains the full LP formulation, embedded demand and lane-cost tables from the original coursework notebook, the solver call, and constraint verification logic. It can be rerun end-to-end to reproduce the `$200,863.75` optimal cost, CVG full utilization, and AFW usage of `38,097` out of `44,350` tons.
