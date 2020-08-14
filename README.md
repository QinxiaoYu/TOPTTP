# TOPTTP

This repository contains the instances and results used in the paper "Team Orienteering with Time-Varying Profit".

Our paper focuses on a variant of the team orienteering problem (TOP) where the profit collected from a visited customer is time-varying. 
In particular, we assume that (i) the profit associated with each customer will decrease with time: the later the vehicle arrives, the less profit will remain; and (ii) the amount of profit collected increases with service time. These two assumptions result in a trade-off between the gains and losses from different customers. The aim of our problem is to determine a set of routes to visit a subset of customers, as well as to decide the duration of service time spent on each visited customer, so as to maximize the total collected profit within a given time limit. We call this problem the TOP with service and arrival time-varying profit (TOP-TTP).

---
## Instances
- [Instances_LDP](./Instances_LDP) includes the instances where the profit of each customer linearly decreases with the arrival time.

- [Instances_EDP](./Instances_EDP) includes the instances where the profit of each customer exponentially decreases with the arrival time.

- [InstanceFileFormat.txt](./InstanceFileFormat.txt) is a description of the text file that defines the network used in each instance.
  - All the networks are modified based on the Solomon benchmark. 
  - Each text file refers to a network with a fixed number of customers located in a specified cluster type. 
  - C (R) refers to the cluster-located network (random-located network).
  - Linearly (exponentially) refer to the profit decreases linearly (exponentially) with the arrival time.
  - L is the perimeter of the minimum bounding rectangle to all nodes in this network.
  - 'CUSTOMER' indicates the node is a customer(1) or a depot (0). In general, the first node denotes the depot, where all vehicles must start and finish. 
  - 'COLLECTRATE' is rate that the collected profit increases with the service time.
  - 'DELAYRATIO' is rate that 'PROFIT' decreases with the arrival time.
  
  ```
    <Instance name>
    <empty line>
    L
    the value of L
    <empty line>
    XCOORD. YCOORD. PROFIT CUSTOMER COLLECTRATE DELAYRATIO
    40	  50	  0	 0	  0	      0	
    45	  68	  10	 1	  0.02	      0.0158	
    ...    
  ```

## Results 

The detailed results listed in the mentioned paper are included in the following two folders.
- [Results_LDP](./Results_LDP) includes the results obtained from different methods for all instances with 6, 9, 25, 50, 75 and 100 customers and linearly decreasing profit. 
- [Results_EDP](./Results_EDP) includes the results obtained from different methods for all instances with 6, 9 and 25 customers and exponentially decreasing profit. 

## Contact Info
Feel free to contact me for more information about our paper via email: Qinxiao Yu (yuqinxiao@tju.edu.cn)

