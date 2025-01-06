# 🔍 Log Analysis with Splunk

## 🚀 Overview
This project demonstrates **log analysis and security event monitoring** using **Splunk**. It focuses on detecting security threats like **brute-force attacks, unauthorized admin access, and web anomalies** using SIEM operations, SPL queries, and real-time alerts.

---

## 🛠 Technologies & Tools Used
| Tool/Technology | Purpose |
|---------------|---------|
| **Splunk** | SIEM & log analysis |
| **Windows Event Logs** | Security logs (e.g., failed logins, brute-force attempts) |
| **Apache Logs** | Web server logs (monitor for anomalies) |
| **PowerShell** | Extract Windows logs |
| **MITRE ATT&CK Framework** | Map threats to known attack techniques |

---

## 🔧 Project Setup

### 1️⃣ Install & Configure Splunk
1. **Download & install Splunk:** [Splunk Download](https://www.splunk.com/en_us/download.html)
2. Start Splunk and log in at `http://localhost:8000/`
3. Add **data sources** for analysis.

### 2️⃣ Collect & Ingest Logs
#### 📂 Windows Security Logs:
- **Extract logs with PowerShell**:
  ```powershell
  Get-EventLog -LogName Security -Newest 1000 | Export-Csv SecurityLogs.csv
