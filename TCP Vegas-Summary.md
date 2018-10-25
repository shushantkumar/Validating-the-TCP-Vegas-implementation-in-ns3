#Brief About TCP Vegas
Tcp Vegas is actually a modification of TCP reno [all changes are only in sending side],but it provides 37 to 71% better throughput with less losses compared to TCP reno.In TCP reno RTT is computed using coarse-grained timer but in TCP vegas RTT is computed using fine-grained timer.

Three techniques that Vegas employs to increase throughput and decrease losses
1. Fast retransmission and Fast recovery
2. Congestion Avoidance Mechanism
3. Modified slow-start Mechanism

### Congestion Avoidance Mechanism
Let BaseRTT to be the RTT of a segment when the connection is not congested. [commonly it is the RTT of the first segment sent by the connection].If we assume that we are not overflowing the connection, then the expected throughput is given by: <br> `Expected = WindowSize/BaseRTT` ,where the windowSize is the size of current congestion window [equal to number of bytes in transmit]. <br><br>
Vegas also calculates the current Actual sending rate.This is done by recording the sending time for a distinguished
segment, recording how many bytes are transmitted between the time that segment is sent and its acknowledgment is
received, computing the RTT for the distinguished segment when its acknowledgment arrives, and dividing the number of
bytes transmitted by the sample RTT. This calculation is done once per round-trip time. <br><br>
By comparing Expected with Actual sending rate vegas will adjust it's window.We will have `Diff = Expected - Actual`,where the Diff is positive or zero by definition.Also we define two thresholds, `α < β` roughly corresponding to having too little and too much extra data in the network, respectively. When `Diff < α` , Vegas increases the congestion window linearly during the next RTT, and when `Diff > β` ,Vegas decreases the congestion window linearly during the next RTT. Vegas leaves the congestion window unchanged when `α< Diff < β`.
