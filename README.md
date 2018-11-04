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

## References
* DCE: https://www.nsnam.org/overview/projects/direct-code-execution/
* Linux Kernel Code: https://elixir.bootlin.com/linux/v4.4/source/net/ipv4/tcp_vegas.c
* TCP Vegas: https://ieeexplore.ieee.org/abstract/document/464716/
* ns-3 code for TCP Vegas (Path: ns-3.xx/src/internet/model/tcp-vegas.{h, cc})
* refer to [Wiki](https://github.com/shushantkumar/Validating-the-TCP-Vegas-implementation-in-ns3/wiki) for more details
