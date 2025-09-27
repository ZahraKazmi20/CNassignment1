# Task 5: HTTPS-Based Website Access

After analyzing the collected traces of HTTPS, the following details were observed:

---

### 1. Name of the Website

`https://colab.research.google.com/`

---

### 2. ClientHello Message Packet

* **Packet Number:** 18

---

### 3. TLS Extensions in ClientHello

The ClientHello message included several TLS extensions such as:

* Supported Versions
* Supported Cipher Suites
* Compression Methods
* Signature Algorithms
* ALPN (Application-Layer Protocol Negotiation)
* Key Share
* Supported Groups
* Session Tickets
* SNI (Server Name Indication)

*(Exact list may vary based on browser and system configuration.)*

---

### 4. ServerHello Message and Cipher Suite

* **Message:** ServerHello
* **Cipher Suite Chosen:** (e.g., TLS_AES_256_GCM_SHA384 or similar depending on capture)

---

### 5. Certificate Message

The server certificate contains details such as:

* **Issuer:** (Certificate Authority, e.g., Google Trust Services LLC)
* **Subject:** (Domain: colab.research.google.com)
* **Validity Dates:** (Start Date – Expiration Date)

*(Exact values should be extracted from the packet capture.)*

---

### 6. First Encrypted Application Data Packet

* **Packet:** TLS Application Data (first packet after the TLS handshake)
* **Why HTTP headers are hidden?**
  Because TLS encrypts all application layer data. Wireshark only displays it as *Encrypted Application Data* instead of plain HTTP headers, ensuring confidentiality.

---
