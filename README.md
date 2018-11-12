# Validating-the-TCP-Vegas-implementation-in-ns3 
​Validate the ns-3 implementation of TCP Vegas

## Description
### Brief
TCP Vegas is a delay based congestion control algorithm which measures per packet RTT to infer the state of congestion in the network. It uses Additive Increase Additive Decrease (AIAD) algorithm to adjust its cwnd. In this project, the aim is to validate ns-3 TCP Vegas implementation by comparing the results obtained from it to those obtained by simulating Linux TCP Vegas

### Required experience
C and C++

## Members
 1. Hardik Rana - 16CO138
 2. Shushant Kumar - 16CO143
 3. Anmol Horo - 16CO206
 
## Mentors
Apoorva Bhargava, Mohit P. Tahiliani

## Implemented Configuration of dumbbell topology
### 1. Configuration 1
In this Configuration of the given dumbbell toplology , the data rate and the delay between the two routers is ``` 150 Mbps ``` and ```0.00075 ms``` respectively. While the data rate between the nodes and the router is ```150 Mbps``` and the delay between the different nodes and the router is the same as in the code provided.<br>
After disabling FACK, the code was executed both with linux and ns3 tcp stack. The result shows that the queue was formed with linux stack but not with ns3 stack.The resultant graphs for this configuration are all present in the folder Configuration1.


### 2. Configuration 2
In this Configuration of the given dumbbell toplology , the data rate and the delay between the two routers is ```1 Mbps``` and``` 0.00075 ms``` respectively. While the data rate between the nodes and the router is ```10 Mbps``` and the delay between the different nodes and the router is the same as in the code provided.<br>
After disabling FACK, the code was executed both with linux and ns3 tcp stack. The result shows that the queue was not formed with both linux and ns3 stack.The resultant graphs for this configuration are all present in the folder Configuration2.


### 3. Configuration 3
In this Configuration of the dumbbell toplology , the data rate and the delay between the two routers is ```1 Mbps``` and    ```50 ms``` respectively. While the data rate between the nodes and the router is ```10 Mbps``` and the delay between the different nodes and the router is the same as in the code provided.<br>
After disabling FACK, the code was executed both with linux and ns3 tcp stack. The result shows that the queue was not formed with both linux and ns3 stack.The resultant graphs for this configuration are all present in the folder Configuration2.


### 4. Configuration 4
In this Configuration of the dumbbell toplology , the data rate and the delay between the two routers is ```200 Kbps``` and ```50 ms``` respectively. While the data rate between the nodes and the router is ```10 Mbps``` and the delay between the different nodes and the router is the same as in the code provided.<br>
After disabling FACK, the code was executed both with linux and ns3 tcp stack. But the result shows that the queue was formed with linux stack but not with ns3 stack.The resultant graphs for this configuration are all present in the folder Configuration4.

### 5. Configuration 5
In this Configuration of the dumbbell toplology , the data rate and the delay between the two routers is ```200 Kbps``` and ```50 ms``` respectively. While the data rate between the nodes and the router is ```1 Mbps``` and the delay between the different nodes and the router is the same as in the code provided.<br>
After disabling FACK and DSACK, the code was executed both with linux and ns3 tcp stack. But the result shows that the queue was formed with linux stack but not with ns3 stack.The resultant graphs for this configuration are all present in the folder Configuration5.

### 6. Configuration 6
We changed value of ```diff``` in ns3 implementaion of TCP Vegas by referring to the linux implementation of TCP Vegas.<br> 
In this Configuration of the given dumbbell toplology , the data rate and the delay between the two routers is ``` 150 Mbps ``` and ```0.00075 ms``` respectively. While the data rate between the nodes and the router is ```150 Mbps``` and the delay between the different nodes and the router is the same as in the code provided.<br>
After disabling FACK, the code was executed both with linux and ns3 tcp stack. The result shows that the queue was formed with linux stack but not with ns3 stack.The resultant graphs for this configuration are all present in the folder Configuration6.

### 7. Configuration 7
We changed value of ```diff``` in ns3 implementaion of TCP Vegas by referring to the linux implementation of TCP Vegas.<br> 
In this Configuration of the dumbbell toplology , the data rate and the delay between the two routers is ```1 Mbps``` and ```50 ms``` respectively. While the data rate between the nodes and the router is ```10 Mbps``` and the delay between the different nodes and the router is the same as in the code provided.<br>
After disabling FACK, the code was executed both with linux and ns3 tcp stack. The result shows that the queue was not formed with both linux and ns3 stack.The resultant graphs for this configuration are all present in the folder Configuration7.





## References
* DCE: https://www.nsnam.org/overview/projects/direct-code-execution/
* Linux Kernel Code: https://elixir.bootlin.com/linux/v4.4/source/net/ipv4/tcp_vegas.c
* TCP Vegas: https://ieeexplore.ieee.org/abstract/document/464716/
* ns-3 code for TCP Vegas (Path: ns-3.xx/src/internet/model/tcp-vegas.{h, cc})
* refer to [Wiki](https://github.com/shushantkumar/Validating-the-TCP-Vegas-implementation-in-ns3/wiki) for more details

