Here are the examiner-optimized, high-scoring solutions for the provided MAKAUT Computer Networks question bank for **Unit 2: Network Layer**. 

---

### **Group A: 1 Mark Questions**
*(Following the strictly required 2–3 lines length rule, emphasizing exact keywords).*

**Q1. Name the three main phases of circuit switching.**
**Answer:** The three main phases are **Connection Establishment** (setup), **Data Transfer**, and **Connection Teardown** (release).

**Q2. What is the fundamental difference between Datagram networks and Virtual-Circuit networks?**
**Answer:** **Datagram networks** route each packet independently using a connectionless approach, whereas **Virtual-Circuit networks** establish a dedicated logical path (connection-oriented) before any data is sent.

**Q3. What is the size of an IPv4 address and an IPv6 address in bits?**
**Answer:** An IPv4 address is **32 bits** long, and an IPv6 address is **128 bits** long.

**Q4. Identify the class of the IPv4 address: 192.168.10.5.**
**Answer:** It belongs to **Class C**, as the first octet (192) falls within the Class C range of 192–223.

**Q5. What is the default subnet mask for a Class B IP address?**
**Answer:** The default subnet mask for Class B is **255.255.0.0** (or `/16` in CIDR notation).

**Q6. What is the purpose of the loopback address 127.0.0.1?**
**Answer:** The loopback address is used for **local host testing** and Inter-Process Communication (IPC); packets sent to this address never leave the local machine's network interface.

**Q7. How is the Network ID calculated given an IP address and its Subnet Mask?**
**Answer:** The Network ID is calculated by performing a **bitwise AND** operation between the given IP address and the Subnet Mask.

**Q8. What does CIDR stand for in IP addressing?**
**Answer:** CIDR stands for **Classless Inter-Domain Routing**, a method that allocates IP addresses flexibly without rigid class boundaries.

**Q9. In a CIDR block represented as /26, how many host addresses are available per subnet?**
**Answer:** A `/26` block leaves 6 bits for hosts ($32 - 26 = 6$). The available usable host addresses are **$2^6 - 2 = 62$ hosts**.

**Q10. What is the minimum and maximum size of the IPv4 header?**
**Answer:** The minimum IPv4 header size is **20 bytes** (when no options are present), and the maximum is **60 bytes** (when the 40-byte options field is fully utilized).

**Q11. Which field in the IPv4 header prevents a packet from wandering endlessly in the network?**
**Answer:** The **Time to Live (TTL)** field prevents endless loops. It is decremented by 1 at each router, and the packet is discarded when TTL reaches 0.

**Q12. What is the purpose of the Fragment Offset field in an IPv4 datagram?**
**Answer:** The **Fragment Offset** indicates the relative position of the current fragment's data in the original, unfragmented datagram, allowing the receiver to reassemble it correctly.

**Q13. True/False: The IPv6 header has a fixed length of 40 bytes.**
**Answer:** **True**. Unlike IPv4, the IPv6 base header is strictly fixed at 40 bytes to speed up router processing.

**Q14. What is an Anycast address in IPv6?**
**Answer:** An **Anycast** address is assigned to a group of interfaces. A packet sent to this address is delivered to the **closest** interface (in terms of routing distance) sharing that address.

**Q15. Which extension header in IPv6 is used for fragmentation?**
**Answer:** The **Fragment Extension Header** is used, as IPv6 strictly dictates that only the source host (not routers) can fragment a packet.

**Q16. Expand the acronym ARP.**
**Answer:** **Address Resolution Protocol**.

**Q17. What is the primary function of the Reverse Address Resolution Protocol (RARP)?**
**Answer:** RARP maps a known physical **MAC address** to an unknown **IP address**, typically used by diskless workstations during bootup.

**Q18. Name the four steps involved in the DHCP configuration process (DORA).**
**Answer:** The four steps are **Discover** (Client), **Offer** (Server), **Request** (Client), and **Acknowledge** (Server).

**Q19. State one major difference between BOOTP and DHCP.**
**Answer:** **BOOTP** requires manual, static binding of MAC to IP addresses by an administrator, whereas **DHCP** assigns IP addresses dynamically from a pool for a leased duration.

**Q20. In what scenario does a router use "Direct Delivery" to forward a packet?**
**Answer:** Direct delivery occurs when the destination host is on the **same physical network** as the deliverer (either the source host or the final router).

**Q21. What is the purpose of a default route (0.0.0.0) in a routing table?**
**Answer:** The **default route** acts as a fallback; if a packet's destination IP does not match any specific entry in the routing table, it is forwarded out this default interface.

**Q22. Differentiate between forwarding and routing.**
**Answer:** **Routing** is the network-wide process of running algorithms to determine optimal paths, while **forwarding** is the local action of a router moving an incoming packet to the correct outgoing port.

**Q23. What is the routing metric used by the Routing Information Protocol (RIP)?**
**Answer:** RIP uses **Hop Count** as its routing metric, with a maximum valid limit of 15 hops.

**Q24. Which algorithm is primarily used by Link State Routing protocols like OSPF?**
**Answer:** Link State protocols utilize **Dijkstra’s Shortest Path** algorithm to compute the best routes.

**Q25. Which routing algorithm relies on the Bellman-Ford equation?**
**Answer:** The **Distance Vector Routing** algorithm (used by RIP) relies on the Bellman-Ford equation.

**Q26. Name the unicast routing protocol used as the inter-domain routing protocol in the Internet (Exterior Gateway Protocol).**
**Answer:** **Border Gateway Protocol (BGP)** is the standard inter-domain routing protocol.

**Q27. Fill in the blank:** In **Circuit** switching, a dedicated path is established before data transfer begins.

**Q28. Fill in the blank:** The **ARP (Address Resolution Protocol)** protocol maps an IP address to a physical (MAC) address.

**Q29. Fill in the blank:** The "count-to-infinity" problem is a severe drawback of **Distance Vector** routing protocols.

**Q30. Fill in the blank:** In IPv4 to IPv6 transition, wrapping an IPv6 packet inside an IPv4 packet is known as **Tunneling**.

---

### **Group B: 5 Marks Questions**
*(Carefully selected fundamental concepts and numericals modeled for maximum university scores).*

**Q1. Compare Circuit Switching and Packet Switching with respect to path establishment, bandwidth reservation, and delay.**
**Introduction**
Circuit Switching and Packet Switching are the two primary methodologies used by the network layer to transfer data between source and destination, differing heavily in resource allocation.

**Main Answer**
| Parameter | Circuit Switching | Packet Switching |
| :--- | :--- | :--- |
| **Path Establishment** | Requires a **dedicated physical path** setup before any data transmission occurs. | No prior path setup. Packets are routed dynamically hop-by-hop. |
| **Bandwidth Reservation** | Bandwidth is **reserved** in advance and remains dedicated for the entire session. | No reservation. Bandwidth is shared dynamically (Statistical Multiplexing). |
| **Delay** | High initial setup delay, but **continuous, negligible delay** during actual data transfer. | No setup delay, but subject to unpredictable **queueing and processing delays** at routers. |
| **Resource Wastage** | High. If the sender pauses, the reserved bandwidth sits idle and is wasted. | Minimal. Resources are heavily optimized and utilized by other packets. |
| **Ideal Application** | Voice communication (Telephone networks). | Data communication (The Internet). |

**Conclusion**
While circuit switching provides guaranteed quality of service suitable for real-time voice, packet switching is vastly superior for bursty data traffic due to its high bandwidth efficiency.

---
**Q4. Explain the concept of Subnetting and Supernetting with suitable examples.**
**Introduction**
Subnetting and Supernetting are two vital IP addressing techniques used to manage the hierarchy and efficiency of the IPv4 address space.

**Main Answer**
*   **Subnetting:**
    *   **Concept:** The process of dividing a single large network into multiple smaller, manageable logical sub-networks (subnets). It is done by borrowing bits from the **Host ID** portion to create a Subnet ID.
    *   **Advantage:** Reduces broadcast traffic, improves security, and organizes network topology.
    *   **Example:** A Class C network `192.168.1.0/24` has 256 IPs. By borrowing 1 bit (new mask `/25`), it splits into two subnets: `192.168.1.0/25` (Hosts 1-126) and `192.168.1.128/25` (Hosts 129-254).
*   **Supernetting (Route Aggregation):**
    *   **Concept:** The exact opposite of subnetting. It combines multiple contiguous small networks into a single large network. It is done by borrowing bits from the **Network ID** portion.
    *   **Advantage:** Drastically reduces the size of routing tables in global routers, speeding up the forwarding process.
    *   **Example:** Four continuous Class C networks (`200.1.0.0/24`, `200.1.1.0/24`, `200.1.2.0/24`, `200.1.3.0/24`) can be aggregated into a single supernet block: `200.1.0.0/22`.

**Conclusion**
Subnetting solves local network congestion by dividing address space, whereas Supernetting solves global router congestion by summarizing address routes.

---
**Q9. Explain the working mechanism of DHCP. How does a client obtain an IP address dynamically?**
**Introduction**
Dynamic Host Configuration Protocol (DHCP) is an application-layer protocol that dynamically assigns IP addresses and network parameters to clients, heavily automating network configuration.

**Main Answer**
DHCP works on a 4-step transaction mechanism widely known as the **DORA process**:
1.  **Discover (DHCPDISCOVER):** A newly booted client has no IP. It broadcasts a DHCP Discover message (`255.255.255.255`) to locate a DHCP server on the network.
2.  **Offer (DHCPOFFER):** Any DHCP server receiving the broadcast checks its pool of available IPs. It responds with an Offer message containing a proposed IP address, subnet mask, and lease duration.
3.  **Request (DHCPREQUEST):** The client may receive multiple offers. It selects one and broadcasts a Request message to formally accept the offered IP, notifying other servers that their offers were rejected.
4.  **Acknowledge (DHCPACK):** The chosen DHCP server finalizes the binding and sends an Acknowledge message containing the final configuration (Default gateway, DNS servers).

**Diagram**
```text
Figure: DHCP DORA Process
[Client]                               [DHCP Server]
   | -------- 1. DHCP DISCOVER (Broadcast) ---> |
   | <------- 2. DHCP OFFER (Unicast/Bcast) --- |
   | -------- 3. DHCP REQUEST (Broadcast) ----> |
   | <------- 4. DHCP ACK (Unicast/Bcast) ----- |
```

**Conclusion**
Through the sequential DORA mechanism, DHCP eliminates the need for manual IP configuration, preventing IP conflicts and ensuring efficient address reuse via leasing.

---
**Q12. Explain the "Count-to-Infinity" problem in Distance Vector Routing. What is the "Split Horizon" solution?**
**Introduction**
The Count-to-Infinity problem is a severe routing loop anomaly native to Distance Vector Routing (like RIP), occurring when a network link fails and routers possess obsolete information.

**Main Answer**
*   **The Problem:** Suppose Router A reaches Router C via Router B. If the link between B and C breaks, B updates its distance to C as infinity. However, before B can broadcast this, A sends its routing table to B, falsely claiming it can reach C in 2 hops. 
*   **The Loop:** B erroneously thinks, "A can reach C, and A is my neighbor, so I can reach C via A in 3 hops." B updates its table. In the next cycle, A sees B's cost increased, so A increases its cost to 4. They continuously bounce updates back and forth, incrementing the metric to infinity.
*   **The Split Horizon Solution:**
    *   **Concept:** The Split Horizon rule states: *"If a router learns a route to a destination from a specific neighbor, it must never advertise that same route back to that neighbor."*
    *   **Application:** In our scenario, since A learned the route to C from B, A will **not** advertise the route for C back to B. 
    *   **Result:** B will not receive the false route from A. B will correctly broadcast the infinity metric, breaking the loop instantly.

**Conclusion**
The count-to-infinity problem causes massive bandwidth wastage. Split Horizon, often combined with Poison Reverse, effectively neutralizes this by enforcing directional constraints on routing updates.

---
**Q14. A host has an IP address of 144.16.74.14 and a subnet mask of 255.255.255.224. Find the Network Address, the Broadcast Address, and the number of valid hosts.**
**Introduction**
To find network parameters, we apply logical bitwise operations between the IP address and the subnet mask, heavily focusing on the "interesting octet" where subnetting occurs.

**Main Answer**
*   **Step 1: Analyze the Mask**
    *   IP Address: `144.16.74.14` (Class B, but custom subnetted).
    *   Subnet Mask: `255.255.255.224` (In binary: `11111111.11111111.11111111.11100000`).
    *   The fourth octet (`224`) is the interesting octet.
*   **Step 2: Find the Block Size (Magic Number)**
    *   Block size = $256 - 224 = \mathbf{32}$.
    *   The subnets increment by 32: `.0, .32, .64, .96, .128...`
*   **Step 3: Determine the Network Address**
    *   Look at the 4th octet of the IP (`144.16.74.14`). The number `14` falls in the first subnet block (0 to 31).
    *   Therefore, Network Address = **144.16.74.0**.
*   **Step 4: Determine the Broadcast Address**
    *   The broadcast address is the last IP before the next subnet begins (`.32`).
    *   Therefore, Broadcast Address = **144.16.74.31**.
*   **Step 5: Calculate Valid Hosts**
    *   Number of host bits (zeros in the mask) = 5.
    *   Usable hosts = $2^5 - 2 = 32 - 2 = \mathbf{30 \text{ hosts}}$.

**Conclusion**
For the given host `144.16.74.14`, the subnet ID is `144.16.74.0`, broadcast is `144.16.74.31`, and it can accommodate a maximum of 30 valid devices.

---
**Q16. An IPv4 datagram has a total length of 4000 bytes and a header of 20 bytes. MTU is 1500 bytes. Show the fragmentation process.**
**Introduction**
Fragmentation occurs when a datagram size exceeds the Maximum Transmission Unit (MTU) of the underlying physical network. Data must be split into chunks whose sizes are multiples of 8 bytes.

**Main Answer**
*   **Given:**
    *   Total Packet = 4000 bytes. Header = 20 bytes. Data Payload = $4000 - 20 = \mathbf{3980 \text{ bytes}}$.
    *   MTU = 1500 bytes. Max Payload per fragment = $1500 - 20 = 1480$ bytes.
    *   Is 1480 divisible by 8? Yes ($1480 / 8 = 185$). So, max data per fragment is 1480.
*   **Fragmentation Breakdown:**
    *   **Fragment 1:**
        *   Data: 1480 bytes (Bytes 0 to 1479).
        *   Total Length: $1480 + 20 = \mathbf{1500 \text{ bytes}}$.
        *   MF Flag: **1** (More fragments follow).
        *   Offset: $0 / 8 = \mathbf{0}$.
    *   **Fragment 2:**
        *   Data: 1480 bytes (Bytes 1480 to 2959).
        *   Total Length: $1480 + 20 = \mathbf{1500 \text{ bytes}}$.
        *   MF Flag: **1** (More fragments follow).
        *   Offset: $1480 / 8 = \mathbf{185}$.
    *   **Fragment 3:**
        *   Remaining Data: $3980 - (1480 + 1480) = \mathbf{1020 \text{ bytes}}$ (Bytes 2960 to 3979).
        *   Total Length: $1020 + 20 = \mathbf{1040 \text{ bytes}}$.
        *   MF Flag: **0** (Last fragment).
        *   Offset: $2960 / 8 = \mathbf{370}$.

**Conclusion**
The original 4000-byte datagram is successfully fragmented into three smaller datagrams of total sizes 1500, 1500, and 1040 bytes respectively to traverse the MTU constraint.

---

### **Group C: 15 Marks Questions**
*(Comprehensive, multi-part university-level answers with complete analytical depth).*

#### **Combination 1: IPv4 Addressing, Subnetting & CIDR**

**Q1(a) Explain Classful IP addressing. Discuss the range, default subnet mask, and application of Class A, B, and C addresses. (5)**
**Introduction**
Before the advent of CIDR, IP addresses were strictly categorized into rigid "classes" to dictate the network and host sizes. This architecture is known as Classful IP Addressing.

**Main Answer**
Classful addressing divides the 32-bit IPv4 address space into 5 classes: A, B, C, D (Multicast), and E (Experimental). The first few bits (leading bits) of the first octet determine the class.
*   **Class A:**
    *   **Leading Bits:** `0`
    *   **Range:** `1.0.0.0` to `126.255.255.255` (`127` is reserved for loopback).
    *   **Default Mask:** `255.0.0.0` (`/8`).
    *   **Application:** Assigned to exceptionally large global organizations or ISPs requiring up to 16 million hosts per network.
*   **Class B:**
    *   **Leading Bits:** `10`
    *   **Range:** `128.0.0.0` to `191.255.255.255`.
    *   **Default Mask:** `255.255.0.0` (`/16`).
    *   **Application:** Utilized by medium-to-large enterprises, universities, and regional networks requiring up to 65,534 hosts.
*   **Class C:**
    *   **Leading Bits:** `110`
    *   **Range:** `192.0.0.0` to `223.255.255.255`.
    *   **Default Mask:** `255.255.255.0` (`/24`).
    *   **Application:** Common in small business and home networks, accommodating a maximum of 254 hosts per network.

**Q1(b) Given IP block 200.150.10.0/24. 4 subnets needed, 30 hosts each. Find subnets, ranges, and masks. (10)**
**Step 1: Determine the New Subnet Mask**
*   The original block is `/24` (Class C), meaning 8 bits are currently available for hosts.
*   We require **4 subnets**. To create 4 subnets, we must borrow $n$ bits from the host portion where $2^n \ge 4$.
*   We borrow **2 bits** ($2^2 = 4$).
*   New Subnet Mask = $/24 + 2 = \mathbf{/26}$.
*   In dotted decimal: $255.255.255.(128+64) \Rightarrow \mathbf{255.255.255.192}$.
*   *Verification Check:* Remaining host bits = $32 - 26 = 6$. Usable hosts = $2^6 - 2 = 62$. This successfully fulfills the requirement of "30 hosts per subnet".

**Step 2: Calculate the Subnet Blocks (Magic Number)**
*   Block Size = $256 - 192 = 64$.
*   The subnets will increment by 64 in the 4th octet:
    *   Subnet 1: `.0`
    *   Subnet 2: `.64`
    *   Subnet 3: `.128`
    *   Subnet 4: `.192`

**Step 3: Evaluate specific queries**
*   **(i) New Subnet Mask:** **255.255.255.192**
*   **(ii) Network address of 1st and 3rd subnets:**
    *   1st Subnet Network ID: **200.150.10.0**
    *   3rd Subnet Network ID: **200.150.10.128**
*   **(iii) First and last usable host IP in the 2nd subnet:**
    *   The 2nd subnet ranges from `.64` (Network) to `.127` (Broadcast).
    *   First usable IP: **200.150.10.65**
    *   Last usable IP: **200.150.10.126**
*   **(iv) Broadcast address of the 4th subnet:**
    *   The 4th subnet starts at `.192` and ends at the boundary of the `/24` block.
    *   Broadcast address: **200.150.10.255**

---

#### **Combination 2: IPv4 Datagram and Fragmentation**

**Q2(a) Draw the neat structure of an IPv4 datagram header and briefly explain the function of each field. (8)**
**Introduction**
The IPv4 datagram header contains vital routing, fragmentation, and quality of service information required by the network layer to successfully deliver packets.

**Header Structure Diagram**
```text
Figure: IPv4 Header Format (20 Bytes without Options)
 0                   15 16                  31
+----+----+------------+----------------------+
|VER |HLEN|   TOS      |     Total Length     |
+----+----+------------+---+---+--------------+
|     Identification   | D | M | Frag Offset  |
+----------------------+---+---+--------------+
|    TTL  |  Protocol  |   Header Checksum    |
+----------------------+----------------------+
|             Source IP Address               |
+---------------------------------------------+
|           Destination IP Address            |
+---------------------------------------------+
|               Options (if any)              |
+---------------------------------------------+
```

**Field Explanations:**
1.  **Version (4 bits):** Identifies the IP version. For IPv4, this is `0100` (4).
2.  **HLEN (4 bits):** Header Length in 32-bit words. Minimum is 5 ($5 \times 4 = 20$ bytes).
3.  **Type of Service (TOS) (8 bits):** Defines packet priority for QoS.
4.  **Total Length (16 bits):** Defines the entire size of the packet (Header + Data) in bytes. Max is 65,535.
5.  **Identification (16 bits):** Unique ID given to a datagram. Highly critical for reassembling fragments.
6.  **Flags (3 bits):** Consists of a reserved bit, DF (Don't Fragment), and MF (More Fragment).
7.  **Fragment Offset (13 bits):** Shows the placement of the fragment data relative to the beginning of the original datagram.
8.  **Time To Live (TTL) (8 bits):** Prevents infinite looping. Router decrements it; discards packet at 0.
9.  **Protocol (8 bits):** Identifies the upper-layer protocol (e.g., TCP=6, UDP=17).
10. **Header Checksum (16 bits):** Detects errors in the header only, not the payload.
11. **Source & Destination IPs (32 bits each):** Sender and receiver addresses.

**Q2(b) Packet arrives: Total Length=5000, HLEN=5, M=1, Offset=100. Evaluate position and payload metrics. (7)**
*   **Step 1: Extract Given Data**
    *   Total Length = 5000 bytes.
    *   Header Length ($HLEN = 5$) = $5 \times 4 = 20$ bytes.
    *   More Fragment bit ($M$) = 1.
    *   Offset = 100.
*   **(i) Is this the first, middle, or last fragment? Justify.**
    *   Because the **Offset is 100** (not 0), it is **not the first fragment**.
    *   Because the **$M$ bit is 1**, there are more fragments coming, meaning it is **not the last fragment**.
    *   *Conclusion:* It is a **Middle Fragment**.
*   **(ii) Calculate the data size of this fragment.**
    *   Data Size = Total Length - Header Size.
    *   Data Size = $5000 - 20 = \mathbf{4980 \text{ bytes}}$.
*   **(iii) What is the byte position of the first and last byte of data?**
    *   The Offset value is expressed in units of 8 bytes.
    *   First Byte Position = Offset $\times$ 8 = $100 \times 8 = \mathbf{800}$.
    *   Last Byte Position = First Byte + Data Size - 1.
    *   Last Byte Position = $800 + 4980 - 1 = \mathbf{5779}$.
    *   *Conclusion:* The payload contained in this fragment spans bytes 800 through 5779 of the original unfragmented message.

---

#### **Combination 4: Unicast Routing - Link State Routing**

**Q4(a) Explain the Link State Routing protocol. Contrast it with Distance Vector Routing. (6)**
**Introduction**
Link State Routing (LSR) is an advanced dynamic routing protocol (e.g., OSPF) where every router constructs a complete, identical map (topology) of the entire network to compute optimal paths.

**Working Principle of LSR:**
1.  **Neighbor Discovery:** Routers send HELLO packets to identify their direct neighbors.
2.  **Cost Measurement:** Routers determine the metric (delay, bandwidth cost) to each neighbor.
3.  **LSP Creation:** The router creates a Link State Packet (LSP) containing its ID, its neighbors' IDs, and the respective costs.
4.  **Reliable Flooding:** LSPs are strictly flooded to *all* routers in the entire network.
5.  **Shortest Path Tree Calculation:** Every router runs Dijkstra’s algorithm independently on the global map to calculate the optimal path to all destinations.

**Contrast with Distance Vector Routing (DVR):**
| Feature | Distance Vector (RIP) | Link State (OSPF) |
| :--- | :--- | :--- |
| **Knowledge** | Shares entire routing table with neighbors. | Shares only local link states with the entire network. |
| **Network View** | Has no concept of full network topology. | Has a complete, 100% accurate topological map. |
| **Algorithm** | Bellman-Ford equation. | Dijkstra’s Shortest Path algorithm. |
| **Convergence** | Slow. Susceptible to routing loops (Count to Infinity). | Fast. Loop-free architecture. |

**Q4(b) Consider a network. Explain how Dijkstra's algorithm finds the shortest path. Construct a graph and trace. (9)**
**Introduction**
Dijkstra's algorithm is an iterative algorithm that finds the shortest path from a source node to all other nodes by maintaining a set of confirmed nodes and updating the cheapest known paths to unconfirmed nodes.

**Sample Graph Construction**
```text
      (2)       (1)
  [A] ---- [B] ---- [C]
   |      /  |       |
(5)|  (2)/   |(3)    |(1)
   |    /    |       |
  [D] ---- [E]-------+
      (1)       (4)
```
*   Let Source Node = **A**. We want to find the shortest path to all nodes (B, C, D, E).

**Algorithm Initialization:**
*   $N'$ = Set of confirmed nodes. Initially, $N' = \{A\}$.
*   $D(v)$ = Current known distance to node $v$.
*   $p(v)$ = Predecessor node along the path to $v$.
*   Init: $D(A)=0$. $D(B)=2$, $D(D)=5$. Others ($\infty$).

**Step-by-Step Trace (Dijkstra's Algorithm):**

| Iteration | Set $N'$ (Confirmed) | $D(B), p(B)$ | $D(C), p(C)$ | $D(D), p(D)$ | $D(E), p(E)$ |
| :---: | :--- | :--- | :--- | :--- | :--- |
| **Init** | {A} | **2, A** | $\infty$ | 5, A | $\infty$ |
| **1** | {A, B} (Pick min D: B=2) | 2, A | **3, B** (2+1)| **4, B** (2+2)| 5, B (2+3) |
| **2** | {A, B, C} (Pick C=3) | 2, A | 3, B | 4, B | **4, C** (3+1) |
| **3** | {A, B, C, D} (Pick D=4) | 2, A | 3, B | 4, B | 4, C (No change) |
| **4** | {A, B, C, D, E} (Pick E=4) | 2, A | 3, B | 4, B | 4, C |

**Final Routing Table for Router A:**
*   To B: Cost = 2 (Next hop: B directly)
*   To C: Cost = 3 (Path: A -> B -> C)
*   To D: Cost = 4 (Path: A -> B -> D)
*   To E: Cost = 4 (Path: A -> B -> C -> E)

**Conclusion**
Dijkstra's algorithm converges with mathematical certainty. By iteratively locking in the absolute shortest path node by node, Link State protocols completely eradicate the routing loop issues found in DVR.
Here is the continuation of the high-scoring, examiner-optimized solutions for the remaining 15-mark questions from **Unit 2: Network Layer**.

---

#### **Combination 3: Unicast Routing - Distance Vector Routing**

**Q3(a) Explain the Distance Vector Routing algorithm in detail. (6)**
**Introduction**
Distance Vector Routing (DVR) is a dynamic, decentralized routing algorithm where each router maintains a table (vector) of minimum known distances to every other node in the network.

**Main Answer (Working Mechanism)**
1.  **Initialization:** Upon booting, a router only knows the cost to its directly connected neighbors. The cost to all other non-adjacent routers is initially set to infinity ($\infty$).
2.  **Information Sharing:** Periodically (e.g., every 30 seconds), every router packages its entire routing table and sends it to its immediate neighbors.
3.  **Routing Table Update:** When a router receives a distance vector from a neighbor, it calculates the new path cost to all destinations using the formula: *Cost to Neighbor + Neighbor's Cost to Destination*.
4.  **Optimal Path Selection:** If the newly calculated cost is strictly less than the currently known cost in its routing table, the router updates its table with the new lowest cost and sets the "Next Hop" to that neighbor.
5.  **Triggered Updates:** If a link fails (cost becomes $\infty$), the router does not wait for the periodic timer; it immediately broadcasts a triggered update to warn neighbors.

**Q3(b) State the Bellman-Ford equation and explain its role in Distance Vector Routing. (4)**
**Answer:** 
The fundamental mathematical core of DVR is the **Bellman-Ford equation**, mathematically represented as:
$$D_x(y) = \min_v \{ c(x,v) + D_v(y) \}$$
**Explanation:**
*   $D_x(y)$ is the least-cost distance from source router $x$ to destination $y$.
*   $v$ represents all adjacent neighbors of $x$.
*   $c(x,v)$ is the physical link cost to reach neighbor $v$.
*   $D_v(y)$ is the known distance from neighbor $v$ to destination $y$.
**Role:** The equation dictates that router $x$ must query all its neighbors ($v$), add the cost of reaching those neighbors, and purely select the mathematical minimum ($\min$) to update its routing table.

**Q3(c) Explain the Routing Information Protocol (RIP). How does it use hop count? What are its limitations? (5)**
*   **Concept:** RIP is an intra-domain (IGP) routing protocol based on the Distance Vector algorithm. It operates over UDP port 520.
*   **Hop Count Metric:** RIP ignores link bandwidth entirely. It uses **Hop Count** as its sole routing metric. Each router traversed counts as 1 hop. 
*   **Infinity Definition:** To prevent infinite loops, RIP strictly defines 16 hops as infinity (unreachable). Thus, the maximum valid path length is 15 hops.
*   **Limitations:**
    *   **Small Network Size:** Because 16 is infinity, RIP is completely useless in large networks spanning more than 15 routers.
    *   **Count-to-Infinity Problem:** Extremely slow to converge during link failures, leading to temporary routing loops.
    *   **Suboptimal Routing:** A 2-hop path over a slow 56Kbps link will incorrectly be preferred over a 3-hop path over 10Gbps fiber optic links.

---

#### **Combination 5: Address Mapping and Host Configuration**

**Q5(a) Describe the frame format of an ARP packet. Explain the step-by-step process of ARP request and reply. (7)**
**Introduction**
The Address Resolution Protocol (ARP) bridges the Network Layer (IP) and Data Link Layer (MAC) by dynamically discovering the MAC address of a destination host on a local network.

**ARP Packet Frame Format:**
```text
 0                   15 16                  31
+----------------------+----------------------+
| Hardware Type (e.g. Ethernet) | Protocol Type (e.g. IPv4) |
+------------+---------+----------------------+
| HLEN (6)   | PLEN(4) |      Operation Code  |
+------------+---------+----------------------+
|           Sender MAC Address (Bytes 0-3)    |
+----------------------+----------------------+
| Sender MAC (4-5)     |    Sender IP (0-1)   |
+----------------------+----------------------+
| Sender IP (2-3)      |  Target MAC (0-1)    |
+----------------------+----------------------+
|           Target MAC Address (Bytes 2-5)    |
+---------------------------------------------+
|           Target IP Address (Bytes 0-3)     |
+---------------------------------------------+
```
*(HLEN: Hardware length, PLEN: Protocol length. Opcode: 1 for Request, 2 for Reply).*

**ARP Process:**
1.  **Cache Check:** The sender checks its local ARP Cache table to see if the target IP-to-MAC mapping already exists.
2.  **Broadcast Request:** If absent, the sender creates an ARP Request packet. The Destination MAC is set to `FF:FF:FF:FF:FF:FF` (Broadcast). The Target MAC field in the payload is left blank (`00:00:00:00:00:00`).
3.  **Network Processing:** Every device on the local network receives and processes the frame. All devices except the target silently discard it.
4.  **Unicast Reply:** The target device recognizes its own IP. It populates its MAC address in the target field, changes the Opcode to 2 (Reply), and sends it as a **Unicast** directly back to the sender.
5.  **Cache Update:** The sender receives the MAC address and updates its ARP cache for future transmissions.

**Q5(b) What is BOOTP? Why was DHCP introduced when BOOTP was present? (3)**
**Answer:** Bootstrap Protocol (BOOTP) is a predecessor to DHCP, used to assign IP addresses to network devices. 
**Why DHCP was introduced:** BOOTP uses **Static Binding**; a network administrator must manually map a device's MAC address to an IP address in the BOOTP server database. With the explosive growth of mobile laptops and large dynamic networks, manual mapping became impossible. DHCP introduced **Dynamic Pools and IP Leasing**, completely automating the IP assignment process.

**Q5(c) Explain the DHCP state transition diagram. How does DHCP handle lease expiration? (5)**
**Main Answer**
DHCP handles IP assignment through states governed by leasing timers:
1.  **Initializing/Selecting:** Client sends DHCPDISCOVER. Server offers an IP (DHCPOFFER).
2.  **Requesting:** Client selects an offer and requests it (DHCPREQUEST).
3.  **Bound State:** Server sends DHCPACK. Client configures its interface and enters the Bound state. It holds the lease for a specified time $T$.
4.  **Renewing State (T1 Timer):** When $50\%$ of the lease time ($T1$) expires, the client sends a unicast DHCPREQUEST to the original server to renew the lease. If acknowledged, timers reset.
5.  **Rebinding State (T2 Timer):** If the original server is dead, the client waits until $87.5\%$ of the lease ($T2$) expires. It then broadcasts a DHCPREQUEST to *any* server to extend the lease.
6.  **Expiration:** If the lease timer reaches 100% without an ACK, the client must immediately drop the IP address and restart from the Initializing state.

---

#### **Combination 6: Delivery, Forwarding and BGP**

**Q6(a) Discuss the different forwarding techniques. Use routing table examples. (8)**
**Introduction**
Forwarding techniques optimize routing tables, shrinking their size from millions of individual host entries to just a few summarized network paths to accelerate router processing speed.

**Main Answer**
1.  **Next-Hop Method:**
    *   Instead of storing the complete route from source to destination, the routing table only stores the IP address of the **immediate next router** (next-hop).
    *   *Example Table:* Destination: `192.168.2.0/24` -> Next Hop: `10.0.0.1`.
2.  **Network-Specific Method:**
    *   Instead of storing an entry for every single host (e.g., PC1, PC2, PC3 on a subnet), the router stores a single entry for the entire destination **Network ID**.
    *   *Example Table:* Destination: `192.168.10.0/24` (Covers all 254 hosts) -> Interface: `eth1`.
3.  **Host-Specific Method:**
    *   Used exceptionally for security or dedicated routing. The table stores a route for one specific target machine using a `/32` subnet mask.
    *   *Example Table:* Destination: `192.168.10.55/32` -> Next Hop: `10.0.0.5`.
4.  **Default Method:**
    *   A catch-all entry. If the destination IP does not match any specific entry in the routing table, the packet is forwarded to the default gateway router.
    *   *Example Table:* Destination: `0.0.0.0/0` -> Next Hop: `192.168.1.254`.

**Q6(b) Write a detailed note on BGP. Why is it a Path Vector Protocol? (7)**
**Introduction**
Border Gateway Protocol (BGP) is an Exterior Gateway Protocol (EGP) used to route data between different Autonomous Systems (AS) on the global Internet.

**Main Answer**
*   **Path Vector Concept:** Unlike Distance Vector protocols that only send a metric (hop count), BGP advertises the **entire path of Autonomous Systems** that a packet must traverse (e.g., Path: `AS100 -> AS200 -> AS300`). 
*   **Loop Prevention:** Because the entire path is attached, if a BGP router sees its own AS number in the incoming path vector, it immediately drops the route, guaranteeing a 100% loop-free global network.
*   **Routing Metrics and Policies:** BGP does not route based purely on link speed (like OSPF) or hop count (like RIP). It routes based on **Policies** set by ISP network admins (e.g., security preferences, peering agreements, or economic routing contracts).
*   **Difference from RIP/OSPF:**
    *   RIP and OSPF are Interior Gateway Protocols (IGPs) used *inside* a single organization.
    *   BGP is an Exterior Gateway Protocol used to connect those organizations globally.

---

#### **Combination 7: IPv6 and Transition Mechanisms**

**Q7(a) Draw the IPv6 base header format and explain its fields. Specifically discuss Traffic Class and Flow Label. (7)**
**Introduction**
The IPv6 header is drastically streamlined compared to IPv4. It has a fixed length of 40 bytes, removing checksums and fragmentation fields from the base header to maximize router processing speed.

**IPv6 Base Header Diagram:**
```text
 0             11             23             31
+----+--------+-------------------------------+
|VER | Traffic|           Flow Label          |
|    | Class  |                               |
+----+--------+---------------+---------------+
|       Payload Length        | Next Header   |
+-----------------------------+---------------+
| Hop Limit   |                               |
+-------------+                               |
|                                             |
|             Source Address (128 bits)       |
|                                             |
+---------------------------------------------+
|                                             |
|           Destination Address (128 bits)    |
|                                             |
+---------------------------------------------+
```
**Explanation of Key Fields:**
*   **Traffic Class (8 bits):** Replaces IPv4 ToS. It assigns priority levels to packets, ensuring critical traffic (like VoIP) avoids congestion drops.
*   **Flow Label (20 bits):** A completely new feature in IPv6. A source tags a sequence of packets (a "flow" like a live video stream) with a unique label. Routers use this label to instantly forward packets without recomputing routing tables, ensuring strict real-time delivery.
*   **Next Header:** Replaces the Protocol field, pointing either to upper-layer protocols (TCP/UDP) or an IPv6 Extension Header.
*   **Hop Limit:** Replaces IPv4 TTL. Decrements by 1 at each router.

**Q7(b) Discuss the concept of Extension Headers in IPv6. (3)**
**Answer:** IPv6 removes "Options" from the base header to keep it a lean 40 bytes. If extra features are needed, they are appended as **Extension Headers** linked between the base header and the payload like a chain. Examples include the *Routing Header* (for strict routing), *Fragment Header* (since routers cannot fragment IPv6, only sources can), and *ESP Header* (for IPsec encryption).

**Q7(c) Explain in detail the tunneling mechanism used to route packets between IPv6 islands. (5)**
**Introduction**
Because the internet cannot switch from IPv4 to IPv6 overnight, transitioning mechanisms are required. Tunneling connects isolated IPv6 networks (islands) separated by legacy IPv4 infrastructure (oceans).

**Mechanism Explanation:**
1.  **Encapsulation:** When an IPv6 packet from "Island A" hits the boundary router to enter the IPv4 internet, the router takes the entire IPv6 packet and wraps it inside the payload of a brand-new **IPv4 packet**.
2.  **Protocol Marking:** The Protocol field of this outer IPv4 packet is set to **41**, signaling to the destination that the payload contains an IPv6 packet.
3.  **Transit:** The packet travels across the global IPv4 internet as a standard IPv4 datagram. Legacy routers are completely unaware of the hidden IPv6 data.
4.  **Decapsulation:** Upon reaching the boundary router of "Island B", the router strips away the IPv4 outer header, extracts the original IPv6 packet, and routes it into the local IPv6 network.

---

#### **Combination 8: Switching and Layer 3 Concepts**

**Q8(a) Compare Circuit Switching, Datagram Packet Switching, and Virtual-Circuit Packet Switching. (8)**
**Main Answer**
| Feature | Circuit Switching | Datagram Packet Switching | Virtual-Circuit Packet Switching |
| :--- | :--- | :--- | :--- |
| **Setup Phase** | Mandatory end-to-end path establishment required. | No setup. Packets are injected instantly. | Mandatory setup of a logical virtual path. |
| **Data Transfer** | Continuous stream of data over a dedicated physical wire. | Packets travel independently; may take different routes. | Packets travel sequentially over the pre-established logical path. |
| **Teardown Phase** | Required to release physical bandwidth. | No teardown required. | Required to clear virtual tables in routers. |
| **Addressing Overhead** | Negligible (only during setup). | High (Every packet must carry full Source & Dest IP). | Low (Packets carry a small Virtual Circuit Identifier - VCI). |
| **Delay** | High setup delay, minimal transfer delay. | No setup delay, high processing/queueing delay. | Moderate setup delay, low processing delay. |
| **Example** | PSTN (Legacy Telephones). | The Internet (IPv4/IPv6). | Frame Relay, ATM, MPLS networks. |

**Q8(b) Write a comprehensive note on RARP. Under what specific physical conditions is RARP utilized? (4)**
**Answer:** The **Reverse Address Resolution Protocol (RARP)** maps a known Physical MAC address to an unknown logical IP address. 
**Physical Condition/Utilization:** RARP is uniquely utilized by **diskless workstations**. When a diskless computer boots up, it knows its MAC address from its hardware NIC, but it has no hard drive to store an operating system or an IP configuration file. It broadcasts a RARP Request (`Target MAC = Own MAC`, `Target IP = ?`). A dedicated RARP server reads the MAC, looks up the corresponding IP in a static table, and sends back the assigned IP address, allowing the device to communicate over TCP/IP.

**Q8(c) Explain how a router makes a routing decision using the longest prefix match algorithm in CIDR. (3)**
**Answer:** In CIDR (Classless Inter-Domain Routing), routing tables often contain overlapping destination subnets. When an incoming packet arrives, the router applies the subnet masks of all matching routes to the destination IP. If multiple routes match, the router uses the **Longest Prefix Match** rule: it strictly selects the routing entry with the highest number of network bits (the largest `/` slash value). 
*Example:* A packet destined for `192.168.1.5` matches both `192.168.1.0/24` and `192.168.1.0/26`. The router selects the `/26` route because 26 bits is a longer, more specific match than 24 bits.
