# run baseline
## aceso
### large: 2nodes 16gpus gpt-13b
```bash
# use torchrun
# modify runtime/scripts/run_gpt_2nodes.sh MASTER_ADDR
# in node1: 
bash runtime/scripts/run_gpt_2nodes.sh 0
# in node2: 
bash runtime/scripts/run_gpt_2nodes.sh 1

# for large, about 366796 ms per iterition training
```
## alpa
## aceso
### large: 2nodes 16gpus gpt-13b
```bash
# use ray
# in node1: 
ray start --head
# in node2: 
join the head node

bash scripts/alpa_gpt_search_execute.sh

## for large, about 10 hours search and execute
```