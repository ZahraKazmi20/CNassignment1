# Task 6: QUIC-Based Website Access

After analyzing the collected traces of QUIC, the following details were observed:

---

### 1. Name of the Website

`https://www.facebook.com/`

---

### 2. Initial QUIC Handshake

* **Packet:** Initial QUIC handshake packet
* **Information Exchanged:**

  * Connection IDs
  * Version negotiation
  * TLS handshake messages (embedded)
  * Transport parameters

---

### 3. QUIC Packet with TLS ClientHello

* **Packet Number:** 247
* This packet contains the first **ClientHello** message (TLS embedded within QUIC).

---

### 4. QUIC Version

* **QUIC Version Used:** IETF QUIC v1

---

### 5. 0-RTT / 1-RTT Keys and Application Data

* **First Application Data Packet (HTTP/3):** Packet #1071 (0-RTT used).
* **Difference vs HTTP over TCP:**

  1. **HTTP/3 over QUIC**:

     * Application data can be sent immediately by the client in the **0-RTT packet (#1071)**.
     * This overlaps with the cryptographic handshake packets (Initial packets like #1069 and #1070).
     * Reduces latency.

  2. **HTTP over TCP (with TLS):**

     * The client must first complete the **TCP handshake (SYN → SYN-ACK → ACK)** and then the **TLS handshake**.
     * Only after multiple round trips can the first HTTP request be sent.
     * Introduces higher latency compared to QUIC.

---
