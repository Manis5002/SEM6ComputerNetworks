Here are the examiner-optimized, high-scoring solutions for the provided MAKAUT Computer Networks question bank for **Unit 3: Transport Layer**.

---

### **Group A: 1 Mark Questions**
*(Following the strictly required 2–3 lines length rule, emphasizing exact keywords).*

**Q1. What is meant by "Process-to-Process Delivery" in the Transport Layer?**
**Answer:** It refers to the delivery of a packet from a specific running application (process) on the source host to the exact corresponding application on the destination host, using port numbers.

**Q2. What is a Socket Address?**
**Answer:** A **Socket Address** is the combination of an IP address and a Port Number (e.g., `192.168.1.5:80`), uniquely identifying a specific process on a specific network node.

**Q3. What is the range of well-known port numbers?**
**Answer:** The well-known port numbers, assigned by IANA for standard universal protocols (like HTTP, FTP), range from **0 to 1023**.

**Q4. Differentiate between multiplexing and demultiplexing at the transport layer.**
**Answer:** **Multiplexing** (sender side) gathers data from multiple applications, adds headers, and sends them over a single network link. **Demultiplexing** (receiver side) reads incoming headers and directs packets to their correct application ports.

**Q5. What is the length of the UDP header?**
**Answer:** The UDP header has a fixed, strictly defined length of exactly **8 bytes**.

**Q6. Name the fields present in a UDP header.**
**Answer:** The four fields (2 bytes each) are: **Source Port**, **Destination Port**, **Total Length**, and **Checksum**.

**Q7. Why does UDP include a pseudo-header in its checksum calculation?**
**Answer:** The pseudo-header (containing Source and Destination IPs) is included to verify that the packet has not been misrouted by the Network Layer and has reached the correct destination host.

**Q8. What is the minimum and maximum size of a TCP header?**
**Answer:** The minimum size is **20 bytes** (no options), and the maximum size is **60 bytes** (with 40 bytes of options).

**Q9. TCP is a "byte-stream" protocol. What does this mean?**
**Answer:** It means TCP does not recognize message boundaries. It views data as a continuous stream of unstructured bytes, numbering each individual byte rather than whole packets.

**Q10. What is the purpose of the Sequence Number field in the TCP header?**
**Answer:** It specifies the byte number of the *first byte* of data in the current TCP segment, enabling the receiver to properly order incoming segments and detect lost data.

**Q11. Which flag in the TCP header is used to initiate a connection?**
**Answer:** The **SYN (Synchronize)** flag is used to initiate a connection and synchronize sequence numbers.

**Q12. Which flag is used to terminate a TCP connection gracefully?**
**Answer:** The **FIN (Finish)** flag is used to smoothly terminate a connection, indicating the sender has no more data to transmit.

**Q13. What is the purpose of the Window Size field in the TCP header?**
**Answer:** It is used for **Flow Control**. It indicates the receiver's available buffer space (in bytes), explicitly telling the sender how much data it can safely transmit.

**Q14. Expand SCTP.**
**Answer:** **Stream Control Transmission Protocol**.

**Q15. State two primary features of SCTP that make it different from TCP.**
**Answer:** Two primary features unique to SCTP are **Multi-homing** (supporting multiple IP addresses per endpoint) and **Multi-streaming** (preventing head-of-line blocking by separating data streams).

**Q16. What is "multihoming" in the context of SCTP?**
**Answer:** Multihoming allows a single SCTP connection to be bound to multiple IP addresses, providing automatic failover if the primary network path goes down.

**Q17. Define Congestion in a computer network.**
**Answer:** Congestion occurs when the number of packets arriving at a network node exceeds its processing or routing capacity, leading to buffer overflows, packet loss, and severe delays.

**Q18. What is the difference between flow control and congestion control?**
**Answer:** **Flow control** prevents a fast sender from overwhelming a *slow receiver* (end-to-end), while **Congestion control** prevents a sender from overwhelming the *underlying network infrastructure* (routers/links).

**Q19. Name the three phases of TCP congestion control.**
**Answer:** The three phases are **Slow Start**, **Congestion Avoidance**, and **Fast Recovery**.

**Q20. What happens to the congestion window (cwnd) threshold when a timeout occurs in TCP?**
**Answer:** In the event of a timeout, the slow-start threshold (`ssthresh`) is reduced to **half** of the current `cwnd`, and the `cwnd` itself is reset to **1 MSS** (restarting Slow Start).

**Q21. Define Quality of Service (QoS).**
**Answer:** QoS refers to a network's ability to provide priority, guaranteed performance levels (throughput, delay, jitter) to specific applications or data flows over others.

**Q22. Name four primary parameters used to measure QoS.**
**Answer:** **Reliability**, **Delay**, **Jitter**, and **Bandwidth**.

**Q23. What is "Jitter" in the context of computer networks?**
**Answer:** Jitter is the **variation in packet delay**. It is the difference in arrival times between consecutive packets, which severely impacts real-time traffic like VoIP.

**Q24. What is the primary purpose of Traffic Shaping?**
**Answer:** Traffic shaping regulates the rate and volume of data entering a network (smoothing out bursty traffic) to ensure it complies with a pre-configured traffic profile, preventing congestion.

**Q25. Which algorithm, Leaky Bucket or Token Bucket, allows bursty traffic?**
**Answer:** The **Token Bucket** algorithm allows bursty traffic up to the maximum capacity of the bucket, whereas Leaky Bucket strictly enforces a constant output rate.

**Q26. Fill in the blank:** TCP uses a **3-Way** Handshake for connection establishment.

**Q27. Fill in the blank:** In TCP, the **Persistence** timer is used to deal with zero-window-size deadlock situations.

**Q28. Fill in the blank:** **Multi-homing** allows an SCTP association to have multiple IP addresses at either end.

**Q29. True/False:** UDP provides reliable and ordered delivery of packets.
**Answer: False**. (It is connectionless and unreliable).

**Q30. True/False:** The Token Bucket algorithm discards packets if the bucket is full.
**Answer: False**. (It discards *tokens* if the bucket is full, not the data packets).

**Q31. True/False:** In the Leaky Bucket algorithm, the output rate is always constant regardless of the input burstiness.
**Answer: True**.

---

### **Group B: 5 Marks Questions**
*(Highly critical concepts and numericals modeled for maximum university scores).*

**Q2. Differentiate between TCP and UDP protocols. Give one real-world application for each.**
**Introduction**
Transmission Control Protocol (TCP) and User Datagram Protocol (UDP) are the foundational Transport Layer protocols, differing radically in reliability and transmission speed.

**Main Answer**
| Feature | TCP (Transmission Control Protocol) | UDP (User Datagram Protocol) |
| :--- | :--- | :--- |
| **Connection Type** | Connection-oriented (Requires 3-way handshake). | Connectionless (No setup required). |
| **Reliability** | Highly reliable. Guarantees delivery via ACKs. | Unreliable (Best-effort). No ACKs. |
| **Ordering** | Guarantees ordered delivery using Sequence Numbers. | No ordering. Packets may arrive out of sync. |
| **Header Size** | Large: 20 to 60 Bytes. | Minimal: Fixed 8 Bytes. |
| **Error/Flow Control** | Strict flow and congestion control algorithms applied. | No flow or congestion control. |
| **Application Example** | **HTTP/HTTPS** (Web browsing), FTP (File transfer). | **VoIP** (Voice calls), DNS, Live Streaming. |

**Conclusion**
TCP trades speed for absolute accuracy (ideal for files/text), whereas UDP trades accuracy for maximum speed (ideal for real-time media).

---
**Q5. Explain the 3-way handshake mechanism used for TCP connection establishment with a neat time-line diagram.**
**Introduction**
To establish a reliable connection, TCP utilizes a highly secure synchronization process called the 3-Way Handshake, ensuring both client and server are ready for data transfer.

**Main Answer**
The process involves exchanging three specific TCP segments:
1.  **Step 1: SYN (Synchronize):** The client wishes to connect. It sends a segment with the SYN flag set to 1. It chooses a random Initial Sequence Number (e.g., Client ISN = 100). No data is sent.
2.  **Step 2: SYN + ACK:** The server receives the SYN. It responds with a segment where both SYN and ACK flags are set to 1. It acknowledges the client's ISN (ACK = 101) and generates its own random ISN (e.g., Server ISN = 500).
3.  **Step 3: ACK (Acknowledge):** The client receives the SYN+ACK. It replies with an ACK segment to acknowledge the server's ISN (ACK = 501). The connection is now formally ESTABLISHED.

**Diagram**
```text
Figure: TCP 3-Way Handshake
   [Client]                                 [Server]
  (CLOSED)                                  (LISTEN)
      |                                         |
      | -------- SYN (Seq=100) ---------------> | (State: SYN-RCVD)
      |                                         |
      | <------- SYN + ACK (Seq=500, Ack=101) - |
      |                                         |
(ESTABLISHED)                                   |
      | -------- ACK (Seq=101, Ack=501) ------> | (State: ESTABLISHED)
      |                                         |
```
**Conclusion**
The 3-way handshake successfully synchronizes sequence numbers in both directions, completely preventing the delivery of duplicated or delayed packets from previous obsolete connections.

---
**Q8. Explain the "Slow Start" and "Congestion Avoidance" phases of TCP Congestion Control.**
**Introduction**
TCP constantly probes the network's bandwidth using dynamic algorithms. Slow Start and Congestion Avoidance are the primary phases controlling the size of the Congestion Window (`cwnd`).

**Main Answer**
**1. Slow Start (Exponential Growth):**
*   **Mechanism:** Despite its name, Slow Start scales extremely fast. It begins with `cwnd = 1 MSS` (Maximum Segment Size).
*   **Growth Rate:** For every single ACK received, `cwnd` increases by 1 MSS. Mathematically, this causes the window size to **double** every Round Trip Time (RTT). (e.g., 1 $\to$ 2 $\to$ 4 $\to$ 8 $\to$ 16).
*   **Termination:** Exponential growth continues until `cwnd` reaches a pre-defined threshold called `ssthresh` (Slow Start Threshold), or a packet loss occurs.

**2. Congestion Avoidance (Linear Growth):**
*   **Mechanism:** Once `cwnd` $\ge$ `ssthresh`, the algorithm assumes the network is approaching its physical limit.
*   **Growth Rate:** To avoid sudden congestion, TCP switches to **Additive Increase**. It increases `cwnd` by only 1 MSS per *entire RTT cycle* (not per ACK). (e.g., 16 $\to$ 17 $\to$ 18 $\to$ 19).
*   **Termination:** Linear growth continues indefinitely until congestion (timeout or 3 duplicate ACKs) is detected.

**Conclusion**
Slow Start rapidly discovers available bandwidth, while Congestion Avoidance cautiously probes the final limits, together ensuring high network utilization without catastrophic collapse.

---
**Q12. Explain the working principle of the Leaky Bucket Algorithm with a suitable diagram.**
**Introduction**
The Leaky Bucket Algorithm is a traffic shaping mechanism used to convert an erratic, bursty incoming data flow into a smooth, steady, and predictable outgoing data stream.

**Main Answer**
*   **Analogy:** Imagine a bucket with a hole at the bottom. Water (data) can be poured into the top in massive, sudden splashes (bursty traffic). However, water only leaks out of the bottom hole at a **strict, constant rate**.
*   **Bucket Capacity:** The bucket has a fixed capacity ($C$). If a burst arrives that is larger than the remaining capacity of the bucket, the excess packets spill over (are completely **dropped** or discarded).
*   **Constant Output:** Regardless of whether the bucket is nearly empty or completely full, the output rate ($\rho$) remains mathematically constant.

**Diagram**
```text
Figure: Leaky Bucket Algorithm
            Bursty Data Packets (Variable Rate)
                      |  |  |  |
                     _V__V__V__V_
                    |            |  <-- Bucket (Capacity C)
                    |  ~~~~~~    |      Drops excess if full
                    |  ~~~~~~    |
                    +----   -----+
                         | |
                         V V
                 Steady Data Stream (Constant Rate)
```
**Conclusion**
By acting as a strictly regulated buffer, the leaky bucket algorithm completely eradicates jitter and burstiness, making it ideal for continuous media streams like VoIP that demand constant bandwidth.

---
**Q14. Token Bucket Numerical: Bucket capacity = 2 MB, Token rate = 200 KBps. Network maximum rate = 1 MBps. How long can a maximum burst of data be transmitted?**
**Introduction**
In the Token Bucket algorithm, a burst can only exceed the token generation rate for a specific duration until the pre-accumulated tokens in the bucket are entirely exhausted.

**Main Answer**
*   **Given Parameters:**
    *   Bucket Capacity ($C$) = 2 MB = **2000 KB** (assuming 1MB = 1000KB for simplicity, or 2048KB. In university exams, $1MB = 1000KB$ is often standard for rates. Let's use 2000 KB).
    *   Token Arrival Rate ($r$) = **200 KBps**.
    *   Maximum Output Rate ($M$) = 1 MBps = **1000 KBps**.
*   **Formula Derivation:** Let $t$ be the maximum burst time. The total data sent out during time $t$ at maximum rate $M$ is $M \times t$.
    This data must be supported by the initial full bucket ($C$) plus the new tokens generated during time $t$ ($r \times t$).
    Therefore: $M \times t = C + (r \times t)$
*   **Calculation:**
    *   $t(M - r) = C$
    *   $t = \frac{C}{M - r}$
    *   $t = \frac{2000}{1000 - 200}$
    *   $t = \frac{2000}{800} = \mathbf{2.5 \text{ seconds}}$
*   **Burst Size Check:** Total data sent = $2.5 \text{ s} \times 1000 \text{ KBps} = 2500 \text{ KB}$ (2.5 MB).

**Conclusion**
The network can sustain transmission at the absolute maximum line speed of 1 MBps for exactly **2.5 seconds** before the bucket is empty and it must throttle down to 200 KBps.

---
**Q15. A computer sends a 5000-byte file via TCP. MSS = 1000 bytes. What are the sequence numbers if the ISN is 1001?**
**Introduction**
TCP is a byte-stream protocol. The sequence number of a segment is always equal to the logical byte number of the very first byte of payload data contained within that segment.

**Main Answer**
*   **Given:** File Size = 5000 bytes, MSS (Data per segment) = 1000 bytes, Initial Sequence Number (ISN) = 1001.
*   The file will be divided into $5000 / 1000 = \mathbf{5 \text{ Segments}}$.
*   **Segment Breakdown:**
    *   **Segment 1:** Carries bytes 1001 to 2000.
        *   **Sequence Number:** **1001**
    *   **Segment 2:** Carries bytes 2001 to 3000.
        *   **Sequence Number:** **2001**
    *   **Segment 3:** Carries bytes 3001 to 4000.
        *   **Sequence Number:** **3001**
    *   **Segment 4:** Carries bytes 4001 to 5000.
        *   **Sequence Number:** **4001**
    *   **Segment 5:** Carries bytes 5001 to 6000.
        *   **Sequence Number:** **5001**

**Conclusion**
The sequence numbers assigned to the five consecutive segments will be 1001, 2001, 3001, 4001, and 5001. The receiving ACK for the final segment would be 6001.

---
**Q16. cwnd is 16 KB, threshold is 8 KB. A timeout occurs. What is the new threshold and cwnd? Trace cwnd for next 5 rounds.**
**Introduction**
A timeout is considered a severe congestion event in TCP (e.g., TCP Reno). The algorithm reacts aggressively by halving the threshold and reverting to the Slow Start phase.

**Main Answer**
*   **Given state prior to Timeout:** `cwnd` = 16 KB, `ssthresh` = 8 KB. (Assuming 1 MSS = 1 KB for tracking).
*   **Reaction to Timeout:**
    1.  **New Threshold (`ssthresh`):** Dropped to half of current `cwnd`.
        $\Rightarrow$ New `ssthresh` = $16 / 2 = \mathbf{8 \text{ KB}}$.
    2.  **New Window (`cwnd`):** Reset strictly to 1 MSS.
        $\Rightarrow$ New `cwnd` = $\mathbf{1 \text{ KB}}$.
*   **Trace for next 5 successful transmission rounds:**
    *   *Round 1:* `cwnd` = 1 KB (Slow Start: Exponential growth begins. Window doubles).
    *   *Round 2:* `cwnd` = 2 KB (Slow Start).
    *   *Round 3:* `cwnd` = 4 KB (Slow Start).
    *   *Round 4:* `cwnd` = **8 KB**. (Threshold reached! Switches to Congestion Avoidance - linear growth).
    *   *Round 5:* `cwnd` = **9 KB**. (Adds 1 MSS per round).

**Conclusion**
Following the timeout, the threshold drops to 8 KB and cwnd drops to 1 KB. By round 5, the cwnd safely recovers linearly to 9 KB.

---

### **Group C: 15 Marks Questions**
*(Comprehensive, multi-part university-level answers with complete analytical depth).*

#### **Combination 1: TCP Connection Management and State Transition**

**Q1(a) Explain the TCP Connection Teardown process (4-way handshake) with a neat diagram. (6)**
**Introduction**
Because a TCP connection is full-duplex (two-way), both sides must terminate their respective data transmission independently. This is achieved via a 4-Way Handshake mechanism using FIN flags.

**Main Answer (Teardown Process)**
1.  **Step 1: FIN from Client:** When the client finishes sending its data, it issues a TCP segment with the FIN (Finish) flag set. It enters the `FIN-WAIT-1` state.
2.  **Step 2: ACK from Server:** The server receives the FIN and immediately acknowledges it with an ACK. The server enters the `CLOSE-WAIT` state. The client, receiving this, moves to `FIN-WAIT-2`. (Note: The server can still send data to the client if needed - this is a "half-close").
3.  **Step 3: FIN from Server:** Once the server finishes transmitting its own remaining data, it sends its own FIN segment to the client and enters the `LAST-ACK` state.
4.  **Step 4: ACK from Client:** The client receives the server's FIN, replies with an ACK, and enters the `TIME-WAIT` state (waiting for 2 Maximum Segment Lifetimes to ensure the ACK isn't lost). The server receives the ACK and closes.

**Diagram**
```text
Figure: TCP 4-Way Connection Teardown
  [Client]                                  [Server]
 (ESTABLISHED)                             (ESTABLISHED)
     | ---------- FIN (I am done) ------------> |
(FIN-WAIT-1)                                    |
     | <--------- ACK (Understood) ------------ | (CLOSE-WAIT)
(FIN-WAIT-2)                                    |
     |                                          |
     | <--------- FIN (I am also done) -------- | (LAST-ACK)
(TIME-WAIT)                                     |
     | ---------- ACK (Goodbye) --------------> | (CLOSED)
(CLOSED)
```

**Q1(b) Discuss the TCP State Transition Diagram (CLOSED, SYN-SENT, SYN-RCVD, ESTABLISHED). (6)**
**Answer:** The TCP state transition diagram is a finite state machine representing the lifecycle of a connection.
*   **CLOSED:** This is the default, inactive state. There is no connection.
*   **Passive vs. Active Open:** A server performs a *Passive Open* (transitions to `LISTEN` state). A client performs an *Active Open* (sends a SYN).
*   **SYN-SENT:** The client enters this state after sending the initial SYN packet. It is waiting for the server's SYN+ACK response.
*   **SYN-RCVD:** The server enters this state after receiving a SYN and sending back a SYN+ACK. It is waiting for the final ACK from the client.
*   **ESTABLISHED:** The steady-state phase. Both client and server enter this state once the 3-way handshake is successfully completed. Data payload can now be exchanged.

**Q1(c) What is the "Silly Window Syndrome" in TCP? (3)**
**Answer:** Silly Window Syndrome is a serious degradation in TCP performance where tiny data segments (e.g., 1 byte of payload inside 40 bytes of header) are constantly exchanged, crippling network efficiency. 
*   **Cause:** It happens if the Sender generates data extremely slowly (1 byte at a time) OR if the Receiver consumes data so slowly that it advertises a window size of 1 byte.
*   **Solution:** Handled by **Nagle's Algorithm** (forces sender to buffer tiny data until MSS is reached or ACK arrives) and **Clark's Solution** (forces receiver to advertise window size of 0 until it can free up at least 1 MSS).

---

#### **Combination 2: TCP Congestion Control (Comprehensive)**

**Q2(a) Discuss TCP Congestion Control in detail (AIMD, Slow Start, Congestion Avoidance). (8)**
**Introduction**
Congestion Control is TCP's mechanism for preventing network collapse by dynamically adjusting the amount of unacknowledged data a sender can inject into the network based on perceived network health.

**Main Answer**
The entire process revolves around a variable called the **Congestion Window (`cwnd`)**. The actual transmission window is strictly: $\min(\text{Receiver Window}, \text{Congestion Window})$.
1.  **Additive Increase Multiplicative Decrease (AIMD):**
    *   This is the core philosophy of TCP.
    *   *Additive Increase:* As long as no packets are lost, increase `cwnd` slowly (linearly) to probe for more bandwidth.
    *   *Multiplicative Decrease:* If congestion (loss) is detected, slash the `cwnd` drastically (by half) to immediately relieve pressure on routers.
2.  **Phase 1: Slow Start:**
    *   Starts with `cwnd` = 1 MSS.
    *   Doubles `cwnd` every RTT (Exponential growth).
    *   Stops when `cwnd` reaches `ssthresh` (Slow Start Threshold).
3.  **Phase 2: Congestion Avoidance:**
    *   Takes over when `cwnd` $\ge$ `ssthresh`.
    *   Increases `cwnd` by exactly 1 MSS per RTT (Linear growth).
    *   Prevents sudden overflow of network buffers.

**Q2(b) Differentiate between Fast Retransmit and Fast Recovery in TCP. (4)**
*   **Fast Retransmit:** Normally, TCP waits for a lengthy Retransmission Timer (RTO) to expire before resending a lost packet. Fast Retransmit bypasses this. If a sender receives **3 duplicate ACKs** for the same sequence number, it assumes the packet was dropped and retransmits it instantly *before* the timer expires.
*   **Fast Recovery:** When 3 duplicate ACKs occur, it indicates mild congestion (since subsequent packets are still arriving to trigger those ACKs). Instead of resetting `cwnd` to 1 (Slow Start), Fast Recovery cuts `ssthresh` in half, sets `cwnd = ssthresh + 3`, and directly enters the Congestion Avoidance phase, ensuring much higher throughput.

**Q2(c) Draw a graph of TCP Congestion Window size versus time. (3)**
```text
Figure: TCP Congestion Window (cwnd) vs Time
cwnd (MSS)
 24 |                          /
 22 |                         /  <-- Congestion Avoidance (Linear)
 20 |                        /     [3 Duplicate ACKs!]
 18 |                       /      |
 16 |       _ ssthresh _   /       v
 14 |      /            --/-----> ssthresh halved (e.g., to 10)
 12 |     /              /|          \ 
 10 |    /              / |           \__ Fast Recovery
  8 |   /              /  |  [Timeout!]
  6 |  /              /   |  |
  4 | /              /    |  v
  2 |/              /     | cwnd drops to 1
  0 +---------------------+-----------------------
      Slow Start   Slow Start      Slow Start
```

---

#### **Combination 3: Quality of Service (QoS) and Traffic Shaping**

**Q3(a) What are the techniques used to improve QoS? Discuss Scheduling, Shaping, and Admission. (6)**
**Introduction**
Quality of Service (QoS) ensures that high-priority applications (like live video) get network priority over delay-insensitive tasks (like email).

**Main Answer**
1.  **Scheduling (Queue Management):**
    *   Routers decide which packet to transmit next.
    *   *FIFO Queuing:* First in, first out. No QoS.
    *   *Priority Queuing:* Packets are grouped by priority class. High-priority queues are emptied completely before low-priority queues are served.
    *   *Weighted Fair Queuing (WFQ):* Different queues get a guaranteed percentage of the bandwidth to prevent starvation of lower priorities.
2.  **Traffic Shaping:**
    *   Implemented at the sender/edge. It smooths out traffic bursts by regulating the flow of packets to match a pre-negotiated rate (Leaky Bucket / Token Bucket).
3.  **Admission Control:**
    *   A preventive mechanism used in Virtual-Circuit networks (like ATM). When a new flow requests a connection, the network calculates if it has enough resources (bandwidth/buffer). If not, the connection is instantly rejected to preserve the QoS of existing connections.

**Q3(b) Explain the Token Bucket Algorithm in detail. How does it allow bursty traffic? (5)**
**Answer:** 
The Token Bucket heavily contrasts with the Leaky Bucket by allowing variable-rate bursts while enforcing an average long-term rate.
*   **Tokens:** A bucket holds a maximum of $C$ tokens. Tokens are generated and added to the bucket at a strictly constant rate of $r$ tokens/second.
*   **Transmission Rule:** To transmit a packet, the sender must remove one token from the bucket. If the bucket is empty, the packet must wait.
*   **Burst Allowance:** If the sender is idle, tokens accumulate up to $C$. When the sender suddenly needs to transmit a massive burst of data, it can rapidly consume all accumulated tokens, sending data at the physical line speed instantly. This perfectly accommodates modern bursty web traffic without losing strict average policing.

**Q3(c) Leaky bucket numerical. Capacity = 1000 packets. Output = 20 packets/sec. Input burst = 150 packets/sec for 5 seconds. Will it overflow? (4)**
*   **Step 1: Calculate Total Incoming Packets**
    Input Rate = 150 pkt/s, Duration = 5 s.
    Total Input = $150 \times 5 = \mathbf{750 \text{ packets}}$.
*   **Step 2: Calculate Packets Processed (Leaked) during Burst**
    Output Rate = 20 pkt/s, Duration = 5 s.
    Total Leaked = $20 \times 5 = \mathbf{100 \text{ packets}}$.
*   **Step 3: Calculate Accumulated Packets in Bucket**
    Accumulated = Total Input - Total Leaked
    Accumulated = $750 - 100 = \mathbf{650 \text{ packets}}$.
*   **Step 4: Check Overflow Condition**
    Bucket Capacity ($C$) = 1000 packets.
    Current Fill = 650 packets. Since $650 < 1000$, the bucket **WILL NOT OVERFLOW**.
    *(Conclusion: The bucket safely absorbs the burst, and will take an additional $650 / 20 = 32.5$ seconds to completely empty).*

---

#### **Combination 5: Transport Layer Timers and Mechanisms**

**Q5(a) TCP uses several timers to ensure reliable data transfer. Explain the purpose of the Retransmission, Persistence, Keepalive, and TIME-WAIT Timers. (8)**
**Main Answer**
1.  **Retransmission Timer (RTO):**
    *   The most crucial timer in TCP. When a sender transmits a segment, it starts this timer. If an ACK is not received before the timer expires, TCP assumes the segment was lost and retransmits it. 
2.  **Persistence Timer:**
    *   Solves the **Zero-Window Deadlock**. If a receiver advertises a window size of 0, the sender stops sending. If the receiver later sends an ACK opening the window, but that ACK is lost, both wait forever. 
    *   The persistence timer forces the sender to periodically send a 1-byte "probe" packet to check if the receiver's window has opened.
3.  **Keepalive Timer:**
    *   Prevents idle connections from wasting server resources indefinitely. If a connection is completely silent for 2 hours, the server sends a probe. If the client fails to respond after multiple probes, the connection is forcefully killed.
4.  **TIME-WAIT Timer:**
    *   Activated during connection teardown. The client waits for $2 \times$ Maximum Segment Lifetime (MSL) before fully closing. This ensures any delayed duplicate packets wandering in the network are naturally dropped, and ensures the server received the final ACK.

**Q5(b) Explain Karn's Algorithm for calculating the Round Trip Time (RTT). Why is it necessary? (4)**
**Answer:** Karn's Algorithm directly addresses the **Retransmission Ambiguity Problem** in calculating dynamic RTO. 
*   **The Problem:** If a sender transmits a packet, the RTO timer expires, it retransmits the packet, and then an ACK finally arrives. Did this ACK belong to the *original* delayed packet or the *retransmitted* packet? There is no way to know. Using this ambiguous RTT will severely skew the timer calculations.
*   **Karn's Solution:** Strictly ignore retransmitted segments when updating RTT estimates. Only calculate RTT for segments that were acknowledged on the very first attempt without retransmission. Furthermore, apply exponential timer backoff upon retransmission.

**Q5(c) What is the purpose of the pseudo-header in UDP? Draw the structure. (3)**
**Answer:** The UDP protocol contains only port numbers, not IP addresses. To guarantee that a packet was not accidentally misrouted by a faulty router (Network Layer), UDP temporarily constructs a 12-byte "pseudo-header" containing the Source IP, Destination IP, and Protocol number. It calculates the checksum over this pseudo-header + UDP header + Data.
```text
Figure: UDP IPv4 Pseudo-Header (12 Bytes)
+---------------------------------------------+
|           Source IP Address (4 Bytes)       |
+---------------------------------------------+
|         Destination IP Address (4 Bytes)    |
+--------+--------+---------------------------+

Here is the continuation and completion of the high-scoring, examiner-optimized solutions for the remaining 15-mark questions from **Unit 3: Transport Layer**.

---

#### **Combination 4: SCTP Architecture and Comparison**

**Q4(a) Describe the packet format and general architecture of the Stream Control Transmission Protocol (SCTP). (6)**
**Introduction**
Stream Control Transmission Protocol (SCTP) is a modern, reliable, message-oriented transport protocol that combines the best features of UDP and TCP while introducing advanced features like multi-homing and multi-streaming.

**Main Answer (Architecture & Format)**
*   **Architecture (Association vs. Connection):** Unlike TCP, which forms a single connection between two IP addresses, SCTP establishes an **Association**. An association can encompass multiple IP addresses at both endpoints (Multi-homing), providing robust failover capabilities.
*   **Streams:** Within one association, data is divided into multiple independent logical **Streams**. If a packet is lost in Stream 1, it only blocks Stream 1. Streams 2 and 3 continue seamlessly, preventing TCP's "Head-of-Line Blocking."
*   **Packet Format:** An SCTP packet does not have a single fixed payload. It consists of a mandatory Common Header followed by one or more highly flexible blocks called **Chunks** (which can carry either control data or user data).

**Diagram: SCTP Packet Structure**
```text
Figure: SCTP Packet Format
+-------------------------------------------------+
|               Source Port (16 bits)             |
+-------------------------------------------------+
|             Destination Port (16 bits)          |
+-------------------------------------------------+
|            Verification Tag (32 bits)           |
+-------------------------------------------------+
|                 Checksum (32 bits)              |
+=================================================+
|   Chunk 1 Type  |  Chunk 1 Flags | Chunk 1 Len  |
+-------------------------------------------------+
|               Chunk 1 Value (Data/Control)      |
+=================================================+
|   Chunk 2 Type  |  Chunk 2 Flags | Chunk 2 Len  |
+-------------------------------------------------+
|               Chunk 2 Value (Data/Control)      |
+-------------------------------------------------+
```
*(The Verification Tag uniquely identifies the association and prevents packet spoofing).*

**Q4(b) How does SCTP's 4-way handshake differ from TCP's 3-way handshake in preventing SYN flooding? (5)**
**Answer:**
*   **TCP SYN Flooding Vulnerability:** In TCP's 3-way handshake, when the server receives a `SYN`, it immediately allocates memory and resources for the connection and replies with a `SYN+ACK`. A malicious attacker can send millions of spoofed `SYN` packets without ever completing the handshake, completely exhausting the server's memory (Denial of Service).
*   **SCTP 4-Way Handshake (State Cookie):** SCTP elegantly solves this by completely delaying resource allocation until the sender is mathematically verified.
    1.  **INIT:** Client sends an INIT chunk.
    2.  **INIT-ACK (with Cookie):** Server receives INIT, but **allocates zero resources**. Instead, it generates a cryptographic **State Cookie** containing all the necessary connection data and sends it back to the client.
    3.  **COOKIE-ECHO:** The client must echo this exact cookie back to the server.
    4.  **COOKIE-ACK:** The server unpacks the cookie, verifies it, *then* allocates memory and responds with a COOKIE-ACK. 
*   **Conclusion:** SYN flooding is impossible in SCTP because a spoofed client will never receive the Cookie and thus can never echo it back, leaving the server's resources entirely safe.

**Q4(c) Compare the Leaky Bucket and Token Bucket algorithms. Can they be combined? If so, how and why? (4)**
**Answer:**
| Feature | Leaky Bucket | Token Bucket |
| :--- | :--- | :--- |
| **Output Rate** | Strictly constant. | Variable (Allows bursts). |
| **Discard Policy** | Drops actual **data packets** if bucket is full. | Discards **tokens**, not data packets. |
| **Use Case** | Shaping (smoothing traffic). | Policing (allowing regulated bursts). |

**Combining Both:** 
Yes, they are highly effective when combined in series. 
*   **How:** The network traffic is first passed through a **Token Bucket**, which allows bursty traffic (like web page loading) up to a maximum limit. The output of the Token Bucket is then fed into a **Leaky Bucket**, which enforces an absolute maximum physical line rate.
*   **Why:** This combination provides the best of both worlds—it grants users the flexibility of bursty transmissions (Token) while mathematically ensuring the network hardware is never overwhelmed beyond its physical capacity limit (Leaky).

---

#### **Combination 6: Deep Dive into TCP Header and Flow Control**

**Q6(a) Draw the complete TCP segment header format and explain the function of the Checksum and Urgent Pointer fields. (6)**
**Introduction**
The TCP header is highly robust, containing sequence tracking, flow control, and error-checking mechanisms to guarantee end-to-end data integrity over the unreliable IP layer.

**Diagram: TCP Segment Header**
```text
Figure: TCP Header Format (20 to 60 Bytes)
 0                   15 16                  31
+----------------------+----------------------+
|     Source Port      |   Destination Port   |
+----------------------+----------------------+
|               Sequence Number               |
+---------------------------------------------+
|            Acknowledgment Number            |
+----+----+--+-+-+-+-+-+----------------------+
|HLEN|Resv|U|A|P|R|S|F|    Window Size        |
+----+----+--+-+-+-+-+-+----------------------+
|       Checksum       |    Urgent Pointer    |
+----------------------+----------------------+
|               Options (if any)              |
+---------------------------------------------+
```

**Field Explanations:**
*   **Checksum (16 bits):** TCP guarantees absolute reliability. The checksum is calculated over three components: the TCP Header, the TCP Payload, and a 12-byte **pseudo-header** (containing IP addresses). If the checksum fails at the receiver, the entire segment is silently discarded, prompting a retransmission.
*   **Urgent Pointer (16 bits):** Used only when the URG flag is set to 1. It indicates that the segment contains highly time-sensitive data (e.g., a user pressing `Ctrl+C` to abort a command). The pointer specifies the exact byte sequence number where the urgent data ends, forcing the receiving application to process this data completely out of sequence.

**Q6(b) Explain how TCP achieves Flow Control using the Sliding Window protocol. Contrast TCP's byte-oriented sliding window with the Data Link Layer's frame-oriented sliding window. (5)**
**Main Answer**
TCP Flow Control ensures a fast sender does not overwhelm the buffers of a slow receiver. It is dynamically managed using the **Window Size** field in the TCP header.
*   **Mechanism:** When the receiver sends an ACK, it also includes its current available buffer space in the Window Size field. If the receiver's application is processing data slowly, the buffer fills up, and the receiver advertises a smaller window. The sender is strictly bounded and can never send more unacknowledged bytes than the advertised window size.
*   **Contrast with DLL Sliding Window:**
    1.  **Unit of Sliding:** In the Data Link Layer, the sliding window operates on discrete **Frames** (e.g., sending Frame 1, 2, 3). In TCP, the window is strictly **Byte-oriented**. It slides based on byte sequence numbers, ignoring segment boundaries.
    2.  **Window Size:** DLL protocols (like Go-Back-N) have a **fixed, static** window size negotiated at setup. TCP uses a **dynamic, variable** window size that expands and shrinks continuously based on the receiver's real-time buffer state.

**Q6(c) Token bucket numerical: Token rate = 10 Mbps, Bucket size = 5 MB. Max line speed = 50 Mbps. What is the max burst size and duration? (4)**
*   **Step 1: Normalize the Units**
    To avoid mathematical errors, convert everything to the same unit (Megabits - Mb).
    *   Token generation rate ($r$) = **10 Mbps**.
    *   Maximum line speed ($M$) = **50 Mbps**.
    *   Bucket capacity ($C$) = 5 Megabytes = $5 \times 8 = \mathbf{40 \text{ Megabits (Mb)}}$.
*   **Step 2: Calculate Duration of Maximum Burst ($t$)**
    The formula for the time $t$ to completely empty a full bucket while generating new tokens is:
    $t = \frac{C}{M - r}$
    $t = \frac{40 \text{ Mb}}{50 \text{ Mbps} - 10 \text{ Mbps}}$
    $t = \frac{40}{40} = \mathbf{1 \text{ second}}$.
*   **Step 3: Calculate the Maximum Burst Size ($S$)**
    The maximum burst size is the total amount of data transmitted at maximum line speed during time $t$.
    $S = M \times t$
    $S = 50 \text{ Mbps} \times 1 \text{ second} = \mathbf{50 \text{ Megabits}}$.
    *(In Megabytes: $50 / 8 = 6.25 \text{ MB}$).*

**Conclusion**
The network can sustain an absolute maximum transmission burst of 50 Megabits (6.25 MB) which will last for exactly 1 second before the sender must slow down to the token generation rate of 10 Mbps.
| All 0s | Proto  |    UDP Length (2 Bytes)   |
+--------+--------+---------------------------+
```
