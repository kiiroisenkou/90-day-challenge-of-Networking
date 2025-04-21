# Day 2: Common Networking Ports, Protocols, and Services

## 🎯 Objectives

- Master the most common networking ports and protocols (TCP/UDP).
- Understand how services like DNS, DHCP, and HTTP operate.
- Use tools like Wireshark, `netstat`, and Nmap to analyze and explore network activity.

---

## 📚 Theoretical Study

- 📺 **Watched**: [CompTIA Network+ (N10-009) - 1.4 - Common Ports and Protocols](https://www.youtube.com/watch?v=xQx2b5oR_gE) by Professor Messer    
- 🧠 **Practiced**: Port/protocol matching quiz from [ExamCompass](https://www.examcompass.com/comptia/network-plus-certification/free-network-plus-practice-tests)

---

## 🧪 Practical Lab

- ✅ Installed **Wireshark** on Ubuntu VM.
- ✅ Captured live traffic while browsing websites (Google, YouTube, etc).
- ✅ Applied packet filters in Wireshark:
  - `tcp.port == 80` (HTTP)
  - `tcp.port == 443` (HTTPS)
  - `udp.port == 53` (DNS)
- ✅ Ran `sudo netstat -an` to analyze active connections and listening ports.
- ✅ Scanned the Ubuntu machine using Nmap:

## 📝 Notes
### 🔢 Common Ports

| Service | Port(s) | Protocol | Use |
|---------|---------|----------|-----|
| HTTP    | 80      | TCP      | Unsecured web traffic |
| HTTPS   | 443     | TCP      | Secure web traffic (SSL/TLS) |
| DNS     | 53      | UDP      | Domain name resolution |
| DHCP    | 67/68   | UDP      | IP address assignment |
| SSH     | 22      | TCP      | Secure remote access |
| FTP     | 20/21   | TCP      | File transfer (unencrypted) |
| SMTP    | 25      | TCP      | Email sending |
| POP3    | 110     | TCP      | Receiving email (downloads to client) |
| IMAP    | 143     | TCP      | Receiving email (syncs with server) |
| Telnet  | 23      | TCP      | Remote terminal access (insecure) |

TCP ensures data is delivered accurately and in order, making it slower due to overhead. 
UDP on the other hand, prioritizes speed, accepting potential data loss for efficiency.

## Use cases
TCP: Best for FTP, HTTP, SMTP, and telnet, where data accuracy is essential.
UDP: Fits DNS queries, streaming, and VoIP, where some data loss is tolerable for speed.
