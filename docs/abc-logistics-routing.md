# ABC Logistics · Fleet routing with delivery windows

ABC Logistics needs to choose routes and assign trucks to them. A low-mileage route can still be infeasible if a truck arrives after the customer’s delivery window or the driver runs out of hours. This WGU business case models that decision for a trucking fleet. The air-cargo project in this repository covers a separate network.

## What the planner would choose

The proposed model chooses which truck serves each route and how much freight each trip carries. Binary route assignments capture the choice to use a truck. Shipment quantities capture how much demand it serves. A mixed-integer linear program lets the planner make both decisions together.

| Component | Meaning for dispatch |
|---|---|
| Objective | Minimize fuel, maintenance and driver costs across the fleet. Fixed per-mile or per-trip rates make the cost terms linear. |
| Capacity | Each assigned load must fit the truck’s weight and volume limits. |
| Service | Each customer must receive its required delivery within its time window. |
| Shift and return | Routes must respect driver-hour limits and end at the depot or designated endpoint. |
| Emissions | If the business sets a CO₂ budget, total modeled emissions must stay within it. |

A short route that misses a delivery window drops out of the feasible set even if its estimated cost is lower. Among the remaining plans, the objective favors lower total operating cost. Turning the proposal into a dispatch schedule would require lane distances, demands, travel times, shift limits, vehicle capacities and cost coefficients. The coursework delivered the formulation and method recommendation. It did not measure savings for ABC Logistics.
