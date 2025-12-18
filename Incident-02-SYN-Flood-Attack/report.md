# Incident Title: SYN Flood Denial of Service Attack

## 1. Summary
Users reported that the company website was inaccessible and displayed a 504 Gateway Timeout error. An investigation revealed abnormal TCP traffic targeting the web server.

## 2. Detection
The incident was detected after multiple users experienced connection timeouts while accessing the website. Network traffic logs were reviewed to identify the cause.

## 3. Analysis
- Protocol: TCP
- Attack Type: SYN Flood (DoS)
- Error Observed: HTTP 504 Gateway Timeout
- Suspicious Activity: Repeated TCP SYN packets without handshake completion

The logs showed that a single IP address repeatedly sent TCP SYN requests to the web server without responding with ACK packets.

## 4. Root Cause
A malicious actor launched a SYN flood attack by sending a large number of TCP SYN packets without completing the three-way handshake. This caused the server to allocate resources for incomplete connections until it became overwhelmed.

## 5. Impact
- Legitimate users were unable to establish connections
- Web server performance degraded
- Website became temporarily unavailable

## 6. Mitigation & Recovery
- Enabled SYN flood protection on firewall
- Implemented rate limiting for TCP connections
- Monitored traffic for abnormal connection attempts

## 7. Lessons Learned
- Importance of DoS protection mechanisms
- Need for continuous network traffic monitoring
- Early detection can reduce service downtime

## 8. Confidence Level
High – Network logs clearly indicate SYN flood behavior.
