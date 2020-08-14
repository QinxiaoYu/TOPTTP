All the networks are modified based on the Solomon benchmark. 

Each text file refers to a network with a fixed number of customers located in a specified cluster type.

The network file format is as follows:

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
  
  - In the 'Instance name':
    - C (R) refers to the cluster-located network (random-located network), following by the number of customers.
    - Linearly (exponentially) refer to the profit decreases linearly (exponentially) with the arrival time.
  - 'L' is the perimeter of the minimum bounding rectangle to all nodes in this network, scaling it then get the time budget for the vehicle.
  - 'CUSTOMER' indicates the node is a customer(1) or a depot (0). In general, the first node denotes the depot, where all vehicles must start and finish. 
  - 'COLLECTRATE' is rate that the collected profit increases with the service time.
  - 'DELAYRATIO' is rate that 'PROFIT' decreases with the arrival time.
  

