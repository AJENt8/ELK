# 📊 Investigating with ELK 

> **Summary:** Learned how to use the Elastic Stack (Elasticsearch, Logstash, Beats, Kibana) to ingest and analyze VPN logs, apply KQL filters, build visualizations, and create dashboards to identify anomalies.

---

## 🎯 Objectives
- Learn Elastic Stack components (Elasticsearch, Logstash, Beats, Kibana)  
- Perform searches and apply filters in Kibana  
- Use **KQL** (Kibana Query Language) for queries with logical operators  
- Investigate VPN logs to identify suspicious activity  
- Create visualizations and build dashboards  

---

## 🛠️ Environment
- Platform: TryHackMe — *Investigating with ELK 101* room  
- Tool: **Elastic Stack** (Elasticsearch + Logstash + Kibana + Beats)  
- Dataset: VPN logs from January 2022 ingested into the `vpn_connections` index  

---

## 🚀 Workflow

### 1) Elastic Stack Overview
- Learned the architecture of Elastic Stack:  
  - **Elasticsearch:** stores and indexes logs  
  - **Logstash:** pipeline for data ingestion and processing  
  - **Beats:** lightweight agents for data shipping  
  - **Kibana:** front-end for visualization and searching  

---

### 2) Kibana Tabs
- **Discover:** searched raw VPN logs, filtered by user and time ranges  
- **Visualization:** built charts and tables to summarize anomalies  
- **Dashboard:** created a dashboard combining saved searches and visualizations  

---

### 3) KQL (Kibana Query Language)
- Practiced two styles of searching:  
  - Free text (broad matches)  
  - Field-based (structured)  
- Used logical operators:  
  - **AND** → combine multiple conditions  
  - **OR** → expand search scope  
  - **NOT** → exclude results  

**Examples:**  
- ```kql
  user.name : "Johny Brown" AND event.outcome : "failure"

---

### 4) VPN Log Investigation Scenario
- Investigated logs in `vpn_connections` index for January 2022
- Key scenario: user Johny Brown (terminated Jan 1) had failed connection attempts post-termination
- Identified anomalous failed login patterns across other users
- Grouped anomalies to detect suspicious activity

---

### 5) Visualization & Dashboard
- Created table and bar chart visualizations for failed logins
- Built a dashboard combining:
  - User login attempts over time
  - Failed logins by username
  - Geographic distribution of VPN connections

## ✅ Outcome
- Successfully investigated VPN logs for anomalies
- Applied KQL filters and logical operators for targeted searches
- Built visualizations and dashboards in Kibana
- Connected log anomalies to a real-world security incident (terminated employee login attempts)

## 🧩 Skills Demonstrated
- Elastic Stack components (Elasticsearch, Logstash, Beats, Kibana)
- Searching/filtering logs with KQL
- Data visualization & dashboard creation
- Investigating anomalous login activity in VPN logs
- SOC analyst mindset for log triage and anomaly detection

  
