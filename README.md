# optEnvelope

## Requires Cobra Toolbox and gurobi solver

## 1. Initialize cobra toolbox and set solver
initCobraToolbox(false) <br />
changeCobraSolver('gurobi','all',0)

## 2. Load model and set desired product
load('iJR904.mat') <br />
desiredProduct='EX_ac_e';

## 3. Run optEnvelope
[main] = optEnvelope(iJR904, desiredProduct,'timeLimit', 600);

## 3.1 Run optEnvelope with mid envelopes
[main, mid] = optEnvelope(iJR904, desiredProduct, 'midPoints', 10)

## 4. Reference
If you use this method or code in your research, please cite our paper:
Motamedian, E., Berzins, K., Muiznieks, R., & Stalidzans, E. (2023). OptEnvelope: A target point guided method for growth-coupled production using knockouts. PLoS ONE, 18(11), e0294313. https://doi.org/10.1371/journal.pone.0294313
