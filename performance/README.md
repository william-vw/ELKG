## Sepsis log

Run the command below to measure query performance:

### Run an individual query
__Sepsis event log__  
`./run.sh -t eye -q ../n3/queries/sepsis_query.n3 -l ../logs/xes/sepsis.ttl -n 5 -r results/sepsis_multi_query.csv -p ../n3/pqn.n3`  

__P2P event log__  
(note - logs/ocel2/ocel2-p2p-expanded.ttl was manually created to include ocel2-p2p.ttl and ocel2-p2p-traces.ttl)  
`./run.sh -t eye -q ../n3/queries/p2p_mav_buying1.n3 -l ../logs/ocel2/ocel2-p2p-expanded.ttl -n 5 -r results/p2p_queries.csv -p ../n3/pqn.n3`  
`./run.sh -t eye -q ../n3/queries/p2p_mav_buying2.n3 -l ../logs/ocel2/ocel2-p2p-expanded.ttl -n 5 -r results/p2p_queries.csv -p ../n3/pqn.n3`  
`./run.sh -t eye -q ../n3/queries/p2p_duplic_paym.n3 -l ../logs/ocel2/ocel2-p2p-expanded.ttl -n 5 -r results/p2p_queries.csv -p ../n3/pqn.n3`  
`./run.sh -t eye -q ../n3/queries/p2p_long_po_approv.n3 -l ../logs/ocel2/ocel2-p2p-expanded.ttl -n 5 -r results/p2p_queries.csv -p ../n3/pqn.n3`  

### Run all constraint queries (N3 file)
`./run_all.sh -t eye -d ../n3/queries/constraints -l ../logs/xes/sepsis.ttl -r results/sepsis_constraints.csv -n 5 -p ../n3/pqn.n3`