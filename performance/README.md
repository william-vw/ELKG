## Sepsis log

### Run individual query
`./run.sh -t eye -q ../n3/queries/sepsis_query.n3 -l ../logs/xes/sepsis.ttl -n 1 -r results/sepsis.csv -p ../n3/pqn.n3`

`./run.sh -t eye -q ../n3/queries/sepsis_query.n3 -l ../logs/xes/sepsis.ttl -n 1 -r results/sepsis.csv -p ../n3/pqn_pred.n3`

### Run all constraint queries (N3 file)
`./run_all.sh -t eye -d ../n3/queries/constraints -l ../logs/xes/sepsis.ttl -r results/sepsis.csv -n 1 -p ../n3/pqn.n3`

`./run_all.sh -t eye -d ../n3/queries/constraints -l ../logs/xes/sepsis_pred.ttl -r results/sepsis_pred.csv -n 1 -p ../n3/pqn_pred.n3`

### Run all constraint queries (PVM file)
Create a PVM file:  
`eye n3/pqn_pred.n3 --turtle logs/xes/sepsis_pred.ttl --image n3/pqn_pred.pvm`

`./run_all.sh -t pvm -d ../n3/queries/constraints -l ../logs/xes/sepsis.ttl -r results/sepsis.csv -n 1 -p ../n3/pqn.pvm`

`./run_all.sh -t pvm -d ../n3/queries/constraints -l ../logs/xes/sepsis_pred.ttl -r results/sepsis_pred_pvm.csv -n 1 -p ../n3/pqn_pred.pvm`