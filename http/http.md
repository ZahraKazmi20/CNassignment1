# Task 4: HTTP-Based Website Access

After analyzing the collected traces of HTTP, the following details were observed:

---

### 1. Name of the Website

`http://httpbin.org/basic-auth/user/passwd`

---

### 2. First GET Request Packet

* **Packet Number:** 182

---

### 3. Headers in the First GET Request

The GET request message contained the following headers and values:

* `Host`: httpbin.org
* `User-Agent`: (browser/client information)
* `Accept`: (content types accepted by client)
* `Accept-Language`: (preferred language, if present)
* `Accept-Encoding`: (compression encodings, if present)
* `Connection`: keep-alive

*(Exact values may vary depending on client/browser used.)*

---

### 4. Status Code in First Server Response

* **401 Unauthorized**

---

### 5. Total HTTP Response Messages

* **Three (3) responses exchanged)**

---

### 6. Connection Persistence

The connection is **persistent**.

* Evidence: The response includes the header `Connection: keep-alive`, which indicates that the TCP connection remains open for multiple requests and responses instead of closing after one exchange.

---
