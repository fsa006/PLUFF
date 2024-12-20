Introduction

The following paper presents the literature research of the authors regarding optimisation and prescriptive analytics applied to several domains of the supply chain. Furthermore, this document illustrates the application of mathematical models using Python (Python Software Foundation., 2024) to provide the optimal solution for a hypothetical business case based on the implementation of a new supply chain network for a contemporary pharmaceutical company. 
The authors investigate the usability of specific models for the network design, like Centre of Gravity for the proposed design of a new supply chain network taking into consideration the business challenges of working with unreliable forecasts, cost constraints and distribution centre location like in the case of launching a new drug to the market. 

Background: New companies deal with bigger challenges than incumbents.

The Challenge: Due to the uncertainty of different factors such as manufacturing/quality issues, 
drug approval date(s), location of the Contract Manufacturing Organisations (CMO), Logistics distribution, contract terms (incoterms) and many other factors that are not in the control of the network designers, the authors have decided to simulate several hypothetical scenarios for the supply network design problems and implement the optimal solution for each of them.

Assumptions from the Supply Chain team/Network designers based on Forecast cases.

-	Low case - Demand Forecast implies a demand where the company is NOT interested in purchasing a warehouse and is outsourcing the logistics services to another company.
-	High case - Demand Forecast implies a demand where the company will need to purchase its own warehouse to manage annual demand and support long-term success.

Id.	Demand Forecast	CMO Location	Incoterms	Warehouse	3PL 
1	Low case	Cork (IE)	EXW	External	Distribution + Warehousing 
2	High case	Cork (IE)	EXW	Internal	Distribution
3	Low/High case	Cork (IE) or Leeds (UK)	CIP	Internal	Distribution
					
Finally, based on the network scenarios defined, the authors have decided the ideal models to provide the optimal solution to each.

**SCENARIO 1. **
Model/Algorithm: ILP. Pyomo, and CBC solver.
Variables: 3PL price and Annual number of trucks.
Objective function: Maximise the number of trucks.
Constraint: Budget.

**SCENARIO 2. **
Model/Algorithm: ILP. Center of gravity.
Variables: Warehouse location.
Objective function: Minimize WH distance from the main hospitals.
Constraint: Distance in Km.

**SCENARIO 3. **
Model/Algorithm: Binary Integer Programming (BIP).
Variables: CMO and WH location. 
Objective function: MAximize Net Present Value (NPV).
Constraint: Capital Available.

Definitions: 

-	3PL: Third Party Logistics.
-	CMO: Contract Manufacturing Organisation. 
-	EXW: Ex Works.
-	CIP: Carriage and Insurance Paid at Place.
-	WH: Warehouse
-	CBC: Coin-or Branch and Cut.

