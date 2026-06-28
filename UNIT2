Here are the examiner-optimized, high-scoring solutions for the provided MAKAUT Computer Networks question bank. 

---

### **Group A: 1 Mark Questions**
*(Following the 2-3 lines length rule for 1-mark questions, focusing on exact keywords).*

**Q1. What are the two main sub-layers of the Data Link Layer (DLL)?**
**Answer:** The Data Link Layer is divided into two sub-layers: **Logical Link Control (LLC)** (handles flow/error control) and **Media Access Control (MAC)** (handles framing and channel access).

**Q2. Define the term 'Framing' in the context of the Data Link Layer.**
**Answer:** **Framing** is the process of grouping a raw stream of bits from the physical layer into manageable, structured data units called **frames**, typically by adding header and trailer bits.

**Q3. State the primary difference between error detection and error correction.**
**Answer:** **Error detection** only identifies whether an error has occurred (e.g., CRC, Parity), whereas **error correction** identifies both the occurrence and the exact bit location of the error to fix it (e.g., Hamming Code).

**Q4. What is the fundamental concept behind block coding?**
**Answer:** The fundamental concept is **redundancy**. In block coding, $k$ data bits are grouped, and $r$ redundant bits are appended to create an $n$-bit codeword ($n = k + r$) to enable error detection or correction.

**Q5. Define Hamming Distance between two codewords.**
**Answer:** **Hamming Distance** is the number of bit positions in which two codewords differ. It is calculated by performing an **XOR** operation between the two words and counting the number of 1s in the result.

**Q6. What is the minimum Hamming distance required to detect $d$ errors?**
**Answer:** To reliably detect $d$ errors, the minimum Hamming distance ($d_{min}$) of the block code must be at least **$d + 1$**.

**Q7. What is the minimum Hamming distance required to correct $d$ errors?**
**Answer:** To successfully correct $d$ errors, the minimum Hamming distance ($d_{min}$) must be at least **$2d + 1$**.

**Q8. Why is modulo-2 arithmetic used in Cyclic Redundancy Check (CRC)?**
**Answer:** **Modulo-2 arithmetic** (using XOR logic) is used because it involves no carries or borrows, making it extremely fast and easy to implement in hardware using basic XOR gates and shift registers.

**Q9. If the generator polynomial in CRC is of degree $n$, what will be the size of the appended CRC bits?**
**Answer:** The size of the appended CRC bits (remainder) will be exactly **$n$ bits**.

**Q10. Name the flow control protocol that uses a sender window of size 1 and a receiver window of size 1.**
**Answer:** The **Stop-and-Wait ARQ** protocol uses a sender window size of 1 and a receiver window size of 1.

**Q11. What is the maximum sender window size in a Go-Back-N (GBN) ARQ protocol using $m$ bits for sequence numbering?**
**Answer:** The maximum sender window size in GBN ARQ is **$2^m - 1$**.

**Q12. What is the required window size for the sender and receiver in Selective Repeat ARQ if $m$ bits are used for sequence numbers?**
**Answer:** Both the sender and receiver window sizes must be **$2^{m-1}$**.

**Q13. Define the concept of 'Piggybacking'.**
**Answer:** **Piggybacking** is a bi-directional data transfer technique where acknowledgment (ACK) bits for received frames are temporarily delayed and attached to outgoing data frames to save bandwidth.

**Q14. Under what condition is piggybacking not useful?**
**Answer:** Piggybacking is not useful (and can degrade performance) when the receiver has **no outgoing data to send**, leading to delayed ACKs and potential sender timeouts.

**Q15. What does the term 'Random Access' mean in MAC protocols?**
**Answer:** **Random Access** (or contention method) means no station is assigned superior rights, and any station can transmit data at any time, which may lead to frame **collisions**.

**Q16. State the vulnerable time for Pure ALOHA if the frame transmission time is $T_f$.**
**Answer:** The vulnerable time for Pure ALOHA is **$2 \times T_f$** (twice the frame transmission time).

**Q17. State the vulnerable time for Slotted ALOHA in terms of frame transmission time $T_f$.**
**Answer:** The vulnerable time for Slotted ALOHA is exactly **$1 \times T_f$** (one frame transmission time).

**Q18. What is the maximum throughput (efficiency) of Pure ALOHA?**
**Answer:** The maximum efficiency of Pure ALOHA is **18.4%** (or $1 / 2e$), occurring when the offered load $G = 0.5$.

**Q19. What is the maximum throughput (efficiency) of Slotted ALOHA?**
**Answer:** The maximum efficiency of Slotted ALOHA is **36.8%** (or $1 / e$), occurring when the offered load $G = 1$.

**Q20. Expand the acronym CSMA/CD.**
**Answer:** **Carrier Sense Multiple Access with Collision Detection**.

**Q21. Expand the acronym CSMA/CA.**
**Answer:** **Carrier Sense Multiple Access with Collision Avoidance**.

**Q22. What is the purpose of the NAV (Network Allocation Vector) in CSMA/CA?**
**Answer:** The **NAV** is a virtual carrier-sensing timer maintained by stations indicating how long the channel will remain busy with current transmissions, preventing them from interrupting.

**Q23. Write the relationship between minimum frame size, transmission rate, and propagation delay in CSMA/CD.**
**Answer:** The minimum frame transmission time ($T_t$) must be at least twice the maximum propagation delay ($T_p$). Formula: **$L / B \ge 2 \times T_p$** (where $L$ = min frame size, $B$ = bandwidth).

**Q24. Why is CSMA/CD not practically implemented in wireless networks?**
**Answer:** In wireless networks, signal attenuation is high. A sending station's own strong signal overwhelms incoming weak signals, making it impossible to listen for collisions simultaneously (**Collision Detection is practically impossible**).

**Q25. Define a 'collision domain'.**
**Answer:** A **collision domain** is a single network segment where data packets can collide with one another when sent simultaneously by different devices (e.g., devices connected to a shared hub).

**Q26. Fill in the blank:** In **Go-Back-N (GBN)** ARQ, if a frame is lost, all subsequent frames sent after that frame are retransmitted.

**Q27. Fill in the blank:** The maximum efficiency of Slotted ALOHA occurs at $G =$ **1**, where $G$ is the offered load.

**Q28. Fill in the blank:** In CSMA/CA, the space between two consecutive frames is called **Inter-Frame Space (IFS)**.

**Q29. True/False:** The receiver window size in Go-Back-N ARQ is always 1.
**Answer: True**.

**Q30. True/False:** Hamming code can only detect errors but cannot correct them.
**Answer: False**. (It is an Error Correcting Code).

**Q31. True/False:** Pure ALOHA requires global time synchronization among all stations.
**Answer: False**. (Slotted ALOHA requires synchronization; Pure ALOHA is unslotted).

**Q32. True/False:** CSMA/CD can detect collisions immediately as they happen on the wired medium.
**Answer: True**. (By monitoring sudden spikes in voltage/energy levels).

---

### **Group B: 5 Marks Questions**
*(Selected critical concepts solved thoroughly to university standards).*

**Q1. Briefly explain the concept of block coding for error detection with a suitable diagram.**
**Introduction**
Block coding is a popular error detection and correction technique utilized in the Data Link Layer to ensure data integrity over noisy channels.

**Main Answer**
*   **Data Grouping:** The sender groups a continuous stream of bits into independent blocks called **Datawords**, each consisting of $k$ bits.
*   **Redundancy Addition:** A block coding algorithm adds $r$ redundant bits to each dataword.
*   **Codeword Generation:** The resulting $n$-bit block ($n = k + r$) is called a **Codeword**.
*   **Transmission:** This $n$-bit codeword is transmitted over the unreliable network channel.
*   **Receiver Logic:** The receiver applies the corresponding decoding algorithm. If the received codeword is mathematically valid, the $k$ data bits are extracted; otherwise, the frame is discarded.

**Diagram**
```text
Figure: Block Coding Concept
      Sender                           Receiver
   +----------+                      +----------+
   | Dataword | (k bits)             | Dataword | (k bits)
   +----+-----+                      +----+-----+
        |                                 ^
        v                                 |
+----------------+               +------------------+
| Generator Algo |               | Checker / Decoder|
+----------------+               +------------------+
        |                                 ^
        v                                 |
   +----------+                      +----------+
   | Codeword | (n = k+r bits) ----> | Codeword | (Received n bits)
   +----------+    Unreliable Link   +----------+
```
**Conclusion**
Block coding converts $k$-bit data into $n$-bit codewords, utilizing redundancy to successfully flag transmission errors at the receiver end.

---
**Q4. Write a short note on the Cyclic Redundancy Check (CRC). How does it utilize polynomial arithmetic?**
**Introduction**
Cyclic Redundancy Check (CRC) is a robust and widely used error-detecting code in local and wide-area networks based on binary polynomial division.

**Main Answer**
*   **Principle:** CRC is based on **modulo-2 binary division**. A fixed redundant string (CRC remainder) is appended to the data so that the resulting frame is perfectly divisible by a predetermined divisor.
*   **Generator Polynomial:** The divisor is represented as an algebraic polynomial with binary coefficients (e.g., $x^4 + x + 1 \Rightarrow 10011$).
*   **Sender Side:** 
    * Append $n$ zero bits to the data (where $n$ is the degree of the polynomial).
    * Divide this augmented data by the generator polynomial using modulo-2 (XOR).
    * The remainder of this division becomes the **CRC bits**.
*   **Receiver Side:** 
    * The receiver divides the incoming frame (Data + CRC) by the exact same generator polynomial.
    * If the **remainder is zero**, the frame is accepted (no error). If non-zero, it is rejected.
*   **Hardware Efficiency:** It is easily implemented in hardware using **linear feedback shift registers (LFSR)** and XOR gates.

**Conclusion**
By mapping bit streams to polynomials and utilizing modulo-2 division, CRC provides highly efficient error detection, particularly for burst errors.

---
**Q6. Differentiate between Go-Back-N ARQ and Selective Repeat ARQ.**
**Introduction**
Both Go-Back-N (GBN) and Selective Repeat (SR) are Sliding Window Protocols used for flow and error control, but they handle frame retransmissions differently.

**Main Answer**
| Feature | Go-Back-N (GBN) ARQ | Selective Repeat (SR) ARQ |
| :--- | :--- | :--- |
| **Retransmission** | Retransmits the lost frame and **all subsequent frames**. | Retransmits **only the specific frame** that was lost or corrupted. |
| **Sender Window Size** | $2^m - 1$ | $2^{m-1}$ |
| **Receiver Window Size** | Exactly **1**. It only accepts frames in sequence. | **$2^{m-1}$**. It can accept and store out-of-order frames. |
| **Bandwidth Efficiency** | Lower efficiency due to redundant retransmission of valid frames. | High efficiency as only erroneous frames consume bandwidth. |
| **Buffer Requirement** | Minimal at receiver (size 1). | High at receiver (requires buffer to sort out-of-order frames). |
| **Complexity** | Simple receiver logic. | Complex logic for sorting and window sliding. |

**Conclusion**
While GBN is simpler and requires less memory, Selective Repeat is heavily preferred in high-error-rate links due to its superior bandwidth conservation.

---
**Q11. Write a short note on CSMA/CD. Explain how a station reacts when it detects a collision.**
**Introduction**
CSMA/CD (Carrier Sense Multiple Access with Collision Detection) is a highly prevalent MAC protocol historically used in wired Ethernet (IEEE 802.3) to manage shared channel access.

**Main Answer**
*   **Carrier Sensing:** Before transmitting, a station "listens" to the channel. If idle, it transmits; if busy, it waits based on its persistence strategy.
*   **Collision Detection:** While transmitting, the station continuously monitors the energy/voltage level of the channel.
*   **Reaction to Collision:** 
    1. **Abort Transmission:** The station instantly halts sending data bits.
    2. **Jamming Signal:** It transmits a short 32-bit to 48-bit **Jam Signal** to ensure all other stations are aware of the collision.
    3. **Exponential Backoff:** The station increments its collision counter ($c$). It then chooses a random number $R$ between $0$ and $2^c - 1$.
    4. **Wait Time:** It waits for a duration equal to $R \times \text{Slot Time}$ before attempting to sense the channel again.
*   **Abort Limit:** If $c$ reaches 16, transmission is permanently aborted, and an error is reported to the upper layers.

**Conclusion**
CSMA/CD prevents channel bandwidth wastage by rapidly aborting collided frames and spacing out retransmissions using the binary exponential backoff algorithm.

---
**Q14. The generator polynomial $G(x) = x^4 + x + 1$ is used for CRC. If the data message is $101101$, calculate the CRC bits that will be appended.**
**Introduction**
CRC is calculated using modulo-2 arithmetic where the generator polynomial acts as the divisor and the data (with appended zeros) acts as the dividend.

**Main Answer**
*   **Step 1: Determine Divisor:** $G(x) = x^4 + 0x^3 + 0x^2 + x^1 + 1 = \mathbf{10011}$.
*   **Step 2: Determine Zeros to Append:** Degree of $G(x)$ is $n=4$. Append 4 zeros to the data. Dividend = $\mathbf{1011010000}$.
*   **Step 3: Modulo-2 Division:**
```text
           101001
      __________________
10011 | 1011010000
        10011
        -----
          10110
          10011
          -----
            10100
            10011
            -----
              1110 (Remainder)
```
*   **CRC Bits:** The remainder is strictly $n=4$ bits. Hence, CRC = **1110**.
*   **Transmitted Message:** Data + CRC = **1011011110**.

**Conclusion**
By performing modulo-2 division, the 4-bit CRC derived is 1110, ensuring successful error detection capabilities for the data frame.

---
**Q17. Prove that in CSMA/CD, the minimum frame transmission time must be at least twice the maximum propagation delay ($T_t \ge 2 \times T_p$).**
**Introduction**
For CSMA/CD to function correctly, a transmitting station must not finish sending its frame before it gets notified of a potential collision at the farthest end of the network.

**Main Answer**
*   **Worst-Case Scenario:** Let Station A and Station B be at the extreme opposite ends of a network. The one-way propagation delay between them is $T_p$.
*   **Timeline:**
    1. At $t = 0$: Station A starts transmitting a frame.
    2. At $t = T_p - \epsilon$: The frame is just about to reach Station B. Station B senses the channel as idle and starts its own transmission.
    3. At $t = T_p$: **Collision occurs** right at Station B.
    4. **Return Journey:** The collision generates a corrupted signal (or jam signal) that must travel all the way back to Station A.
    5. At $t = 2 \times T_p$: The collision signal reaches Station A.
*   **Requirement:** If Station A finishes transmitting its frame *before* $2 \times T_p$, it will assume the frame was sent successfully and won't detect the collision. 
*   **Proof Conclusion:** Thus, Station A must continue transmitting for at least $2 \times T_p$. Therefore, Minimum Transmission Time ($T_t$) $\ge 2 \times T_p$.

**Conclusion**
This fundamental relation ($T_t \ge 2 \times T_p$) is the foundational rule that dictates the minimum frame size (e.g., 64 bytes in Ethernet) relative to network length.

---

### **Group C: 15 Marks Questions**
*(Comprehensive, university-grade long answers with diagrams).*

#### **Combination 3: Flow Control Protocols & Efficiency Analysis**
**Q3(a) Derive the expression for link utilization (efficiency) of the Stop-and-Wait ARQ protocol. (5)**
**Introduction**
Efficiency or Link Utilization ($\eta$) represents the fraction of time the sender is actually transmitting useful data compared to the total cycle time required to send one frame and receive its acknowledgment.

**Main Answer**
*   Let $T_t$ = Transmission time of the data frame.
*   Let $T_p$ = Propagation delay (time taken for a bit to travel from sender to receiver).
*   Let $T_{ack}$ = Transmission time of the ACK frame. (Usually very small, assumed $\approx 0$).
*   Let $T_{proc}$ = Processing delay at receiver. (Assumed $\approx 0$).
*   **Total Cycle Time:** The total time required to successfully deliver one frame and receive its ACK is:
    $\text{Total Time} = T_t (\text{Data}) + T_p (\text{Data travel}) + T_{ack} + T_p (\text{ACK travel})$
    $\text{Total Time} \approx T_t + 2T_p$
*   **Useful Time:** The time spent putting useful data onto the link is simply $T_t$.
*   **Efficiency Formula:**
    $\eta = \frac{\text{Useful Time}}{\text{Total Cycle Time}}$
    $\eta = \frac{T_t}{T_t + 2T_p}$
*   Dividing numerator and denominator by $T_t$, we introduce the variable $a = \frac{T_p}{T_t}$:
    **$\eta = \frac{1}{1 + 2a}$**

**Q3(b) A satellite channel operates at 2 Mbps with a propagation delay of 250 ms. Frame size is 1000 bytes. Calculate maximum link utilization for Stop-and-Wait ARQ. (5)**
*   **Given:**
    *   Bandwidth ($B$) = 2 Mbps = $2 \times 10^6$ bps
    *   Propagation Delay ($T_p$) = 250 ms = $0.25$ seconds
    *   Frame Size ($L$) = 1000 bytes = $1000 \times 8 = 8000$ bits
*   **Step 1: Calculate Transmission Time ($T_t$)**
    $T_t = \frac{L}{B} = \frac{8000}{2 \times 10^6} = 0.004 \text{ seconds (4 ms)}$
*   **Step 2: Calculate variable '$a$'**
    $a = \frac{T_p}{T_t} = \frac{250 \text{ ms}}{4 \text{ ms}} = 62.5$
*   **Step 3: Calculate Efficiency ($\eta$)**
    $\eta = \frac{1}{1 + 2a} = \frac{1}{1 + 2(62.5)} = \frac{1}{1 + 125} = \frac{1}{126}$
    $\eta = 0.00793$ or **0.793%**
*   **Conclusion:** The efficiency is extremely poor (~0.79%) because the frame transmission time is tiny compared to the massive satellite propagation delay.

**Q3(c) To achieve 100% utilization, what should be the sender window size if we switch to Go-Back-N ARQ? (5)**
*   **Explanation:** In sliding window protocols like GBN, the sender can transmit a window of $W$ frames before stopping to wait for an ACK.
*   **Efficiency for GBN:** $\eta = \frac{W}{1 + 2a}$
*   **Condition for 100% Utilization:** To keep the channel full, $\eta$ must be 1.
    $1 = \frac{W}{1 + 2a} \implies W = 1 + 2a$
*   **Calculation:**
    $W = 1 + 2(62.5) = 1 + 125 = \mathbf{126}$
*   **Conclusion:** The sender window size must be at least **126 frames**. The sequence number bits required would be $m=7$ bits (since $2^7-1 = 127 \ge 126$).

---

#### **Combination 7: CSMA/CD Protocol and Network Design**
**Q7(a) Explain the complete working mechanism of CSMA/CD with a neat flowchart. (7)**
**Introduction**
Carrier Sense Multiple Access with Collision Detection (CSMA/CD) is designed to mitigate the severe bandwidth loss caused by collisions in random access networks. 

**Main Answer (Working Mechanism)**
1.  **Carrier Sensing:** A station wanting to transmit checks the medium. If the channel is busy, it waits (usually 1-persistent strategy in Ethernet).
2.  **Transmission & Monitoring:** When the channel is idle, the station begins transmitting the frame while simultaneously monitoring the channel's energy levels to detect a collision.
3.  **Collision Detection:** If the monitored voltage spike indicates a collision, the station acts immediately.
4.  **Jam Signal:** The station halts transmission and sends a 48-bit jam signal to artificially prolong the collision state, ensuring all other stations detect it.
5.  **Backoff Algorithm:** The station executes the **Binary Exponential Backoff algorithm**:
    *   Increments collision counter $c$.
    *   If $c = 16$, it drops the frame (max tries reached).
    *   Calculates a random number $R \in [0, 2^c - 1]$.
    *   Waits for $T_B = R \times \text{Slot Time}$.
6.  **Retransmission:** After waiting, it restarts the carrier sensing phase.

**Flowchart Diagram**
```text
Figure: CSMA/CD Flowchart
       [Start]
          |
          v
   [Sense Channel] <--------------------+
          |                             |
     Busy?+---(Yes)---> [Wait] ---------+
          |
        (No)
          v
 [Transmit Data & Monitor]
          |
    Collision Detected?
          |
        (Yes)                           (No)
          |                               |
          v                               v
[Send Jam Signal]                  [Transmission Success]
          |                               |
          v                            [End]
[Increment c (c = c+1)]
          |
     Is c == 16? --(Yes)--> [Abort & Report Error]
          |
        (No)
          v
[Select R from 0 to 2^c-1]
          |
[Wait for R * Slot Time]
          |
          +-----------------------------+
```

**Q7(b) Why is there a minimum frame size requirement in CSMA/CD? (3)**
**Answer:** The minimum frame size requirement ensures that a station's transmission lasts long enough for a collision signal from the farthest end of the network to travel back to the sender. If the frame is too small, the sender finishes transmitting before the collision notification arrives, falsely assuming successful delivery.

**Q7(c) Calculate the minimum frame size in bytes required for collision detection. (5)**
*   **Given:**
    *   Bandwidth ($B$) = 10 Mbps = $10^7$ bps
    *   Distance ($d$) = 2 km = 2000 m
    *   Speed ($v$) = $2 \times 10^8$ m/s
*   **Step 1: Calculate Propagation Delay ($T_p$)**
    $T_p = \frac{\text{Distance}}{\text{Speed}} = \frac{2000}{2 \times 10^8} = 10^{-5} \text{ seconds (10 }\mu\text{s)}$
*   **Step 2: Apply CSMA/CD condition**
    $T_t \ge 2 \times T_p$
    $\frac{L}{B} \ge 2 \times T_p$
*   **Step 3: Calculate Minimum Length ($L$)**
    $L \ge 2 \times T_p \times B$
    $L \ge 2 \times 10^{-5} \times 10^7$
    $L \ge 2 \times 100 = \mathbf{200 \text{ bits}}$
*   **Step 4: Convert to Bytes**
    Minimum Frame Size = $200 / 8 = \mathbf{25 \text{ bytes}}$.
*   **Conclusion:** The minimum frame size required for the network is 25 bytes. (Note: Ethernet standard forces a 64-byte minimum for practical safety margins).

---

#### **Combination 8: Wireless MAC and CSMA/CA**
**Q8(a) Discuss the Hidden Station and Exposed Station problems in wireless networks. (6)**
**Introduction**
Unlike wired networks, wireless signals suffer from rapid attenuation and line-of-sight obstructions, leading to severe MAC-level vulnerabilities known as Hidden and Exposed Station problems.

**Main Answer**
**1. The Hidden Station Problem:**
*   **Concept:** Two stations are hidden from each other but can both transmit to a common central receiver.
*   **Scenario:** 
    * Station A can hear Station B. Station C can hear Station B. 
    * However, A and C **cannot** hear each other (they are out of range).
*   **The Issue:** A starts sending data to B. C, not sensing A's signal, assumes the medium is free and also transmits to B. 
*   **Result:** The signals from A and C violently collide at B, destroying both frames. A and C are "hidden" from each other.

**2. The Exposed Station Problem:**
*   **Concept:** A station is forced to unnecessarily wait because it is "exposed" to a neighboring transmission that actually will not interfere with its own target.
*   **Scenario:** 
    * A transmits to B. 
    * C (close to B) hears the transmission and wants to transmit to D (which is far from B).
*   **The Issue:** C carrier-senses the medium, hears A's transmission to B, and incorrectly assumes it must wait.
*   **Result:** Massive waste of bandwidth, as C transmitting to D would not have caused a collision at B.

**Q8(b) Explain how the CSMA/CA protocol mitigates these problems using IFS, Contention Window, RTS, CTS, and ACK. (9)**
**Introduction**
CSMA/CA (Carrier Sense Multiple Access with Collision Avoidance), defined in IEEE 802.11, avoids collisions actively rather than detecting them, resolving hidden node issues using control frames.

**Main Answer**
**1. Collision Avoidance Mechanisms:**
*   **Inter-Frame Space (IFS):** Even if the channel is idle, a station must wait for an IFS duration. High-priority frames wait for a short IFS (SIFS), while regular data waits for a distributed IFS (DIFS).
*   **Contention Window (CW):** After DIFS, the station enters a backoff period. It picks a random slot in the contention window and counts down only when the channel is idle. This heavily avoids simultaneous starts.

**2. Mitigating Hidden/Exposed Node using RTS/CTS:**
CSMA/CA uses a four-way handshake (RTS-CTS-Data-ACK) to reserve the channel globally.
*   **RTS (Request to Send):** Sender sends a tiny RTS frame to the receiver. It includes a duration value indicating how long the transmission will take.
*   **CTS (Clear to Send):** If ready, the receiver broadcasts a CTS frame containing the same duration. 
*   **The Magic of NAV (Network Allocation Vector):** 
    * Any "hidden" station (like C) hears the CTS from the receiver, reads the duration, and updates its NAV timer, going to sleep. This solves the **Hidden Node** problem.
    * An "exposed" station hears the RTS but NOT the CTS, realizes the receiver is out of range, and is free to transmit. This solves the **Exposed Node** problem.
*   **ACK (Acknowledgment):** Upon successful receipt of data, the receiver waits for SIFS and sends an ACK. Due to the high error rates of wireless links, the ACK is strictly mandatory.

**Diagram**
```text
Figure: CSMA/CA RTS/CTS Handshake
Sender                                  Receiver
  | -------- RTS (Req to Send) -------->   |
  |                                        |
  | <------- CTS (Clear to Send) -------   | (CTS also heard by Hidden Nodes)
  |                                        |
  | =============== DATA ===============>  |
  |                                        |
  | <------- ACK (Acknowledgment) ------   |
  |                                        |
```
**Conclusion**
By replacing reactive collision detection with proactive collision avoidance and virtual carrier sensing (NAV), CSMA/CA provides stable and efficient medium access in complex wireless environments.
