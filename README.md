# **Sality P2P Botnet PCAP Collection**

![Sality Botnet](https://example.com/sality-image.png)  
*(Replace with a relevant image or remove this section if unnecessary)*  

This repository contains **packet capture (PCAP) files** collected from four virtual machines (**VMs**) that were part of an active **Sality Peer-to-Peer (P2P) botnet**. The network traffic was recorded in a controlled malware analysis testbed (**MALBED**) to support research on botnet behavior, P2P communication patterns, and intrusion detection.

---

## 📌 Overview

This dataset was collected to analyze **Sality botnet P2P communication** and provide researchers with real-world malicious network traffic. The captured traffic includes:

- **Infected node interactions**
- **P2P command-and-control (C2) communications**
- **Botnet propagation activities**

### 🔥 Potential Use Cases
✅ Reverse engineering **Sality's P2P network**  
✅ Identifying **malicious network behavior**  
✅ Evaluating **intrusion detection strategies**  
✅ Developing **machine learning-based botnet detection models**  

---

## 🔍 Usage & Analysis

Researchers and cybersecurity practitioners can analyze the PCAP files using tools such as:

- **Wireshark** – for protocol analysis and packet inspection
- **Zeek (Bro)** – for network traffic analysis
- **Snort / Suricata** – for IDS rule validation
- **Python (Scapy / Pyshark)** – for custom parsing and feature extraction

### **Example Analysis Commands**
#### Using `tshark` to filter specific traffic:
```bash
tshark -r vm1.pcap -Y "ip.src == x.x.x.x && ip.dst == y.y.y.y"
```
*(Replace `x.x.x.x` and `y.y.y.y` with IP addresses of interest.)*

#### Using `Zeek` to extract network behavior:
```bash
zeek -r vm1.pcap
cat conn.log | awk '{print $1, $2, $3, $4}'
```

#### Using `Scapy` in Python:
```python
from scapy.all import rdpcap

packets = rdpcap("vm1.pcap")
for pkt in packets:
    if pkt.haslayer("IP"):
        print(pkt.summary())
```

---

## ⚠️ License & Ethical Considerations

🚨 **This dataset is for research and educational purposes only.**  
❌ **Do not use it for malicious purposes or unauthorized network activity.**  
✅ **Follow ethical guidelines and legal regulations when analyzing this data.**  

---

---

## 📩 Contact

For inquiries or collaboration opportunities, please reach out:  

📧 **pmithiiran@gmail.com** 

---

**🔒 Security Notice:**  
This dataset contains **real malicious traffic** from a controlled environment. **Do not execute PCAP files in an unprotected network!** Always analyze them in an **isolated or sandboxed environment**.

---

🚀 **Enjoy researching, and stay secure!**  
