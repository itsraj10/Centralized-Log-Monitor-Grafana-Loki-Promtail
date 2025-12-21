# Centralized Live Log Monitoring with Grafana, Loki & Promtail 🚀

📌 Overview
This project implements a **production-ready centralized log monitoring system**
where logs from **multiple Linux & Windows servers** are collected on a central server
and visualized in a **human-friendly Grafana UI**.

![Architecture](https://github.com/user-attachments/assets/6ac126ec-9d28-4314-8445-45204c509ede)

All logs from multiple **Linux and Windows production servers** are collected on a
central log server and visualized through a **clean, human-readable Grafana UI**.

The solution is designed for **real production use!!!

<img width="1400" height="458" alt="image" src="https://github.com/user-attachments/assets/f4252351-4464-4714-ab54-11c2253b6a9b" />

____________________________________________________________________________________________________________________________

The solution is:
- ✅ Centralized logging for all servers
- ✅ Works 24/7 on a single log server
- ✅ Click server IP → logs appear instantly
- ✅ No modification or deletion of existing logs
- ✅ Zero data loss

____________________________________________________________________________________________________________________________

🧠 Real-World Problem Solved
In production environments, troubleshooting becomes difficult when:
- Logs are spread across many servers
- Manual SSH access is required
- Non-technical teams cannot view logs easily

____________________________________________________________________________________________________________________________

🛠 How I Implemented This (Step-by-Step Summary)

Step 1 — Central Log Collection
All production server logs (Linux & Windows) are already forwarded to a central server
using an existing pipeline.

Log structure on the central server: /var/log/blrserverlogs/<SERVER_IP>/YYYY/MM/DD/*.log

Step 2 — Installed Loki (Log Storage)
- Installed Loki on the central log server
- Configured filesystem-based storage
- Enabled indexing based on timestamps and labels
- Ensured Loki runs as a systemd service (24/7)
  

Step 3 — Installed Promtail (Log Shipper)
- Configured Promtail to **read existing log files only**
- Extracted `server_ip` dynamically from folder structure
  

Step 4 — Installed Grafana (Visualization)
- Installed Grafana on the same server
- Added Loki as a data source
- Created dashboards using Logs panel
- Enabled:
- Infinite scrolling
- Auto refresh
- Human-readable formatting

Step 5 — Dashboard Design (Zero Query UI)
- Created a **Server IP dropdown** using Grafana variables
- Users select a server IP → logs appear automatically
- No manual query typing required

Step 6 — Live Troubleshooting
- Used Grafana **Explore mode** for real-time log streaming
- Supports **live tail** for instant debugging
- Filtered by server IP for targeted troubleshooting.

____________________________________________________________________________________________________________________________

💁 Why This Project
This project reflects **real-world DevOps and SRE practices**:
- Simple
- Stable
- Production-safe
- Easy to operate
____________________________________________________________________________________________________________________________

⏳ Status

✅ Implemented  
✅ Working in production  
✅ Running 24/7 

![Screenshot 2025-12-21 at 7 19 15 PM](https://github.com/user-attachments/assets/002ae2ba-6851-4fcc-b480-5fe12ae60c43)


____________________________________________________________________________________________________________________________

📌 Why I made this:-

I built this project to give my team a single, reliable, and human-friendly view of production logs, enabling faster troubleshooting, better visibility, and safer operations — without disrupting existing systems.
And my team is currently using this.

❤️ I wanted to share this project with you all, and I hope you were able to learn something useful from it.

____________________________________________________________________________________________________________________________
