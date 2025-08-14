# Task 7 – Monitor System Resources Using Netdata
## 📌 Objective

Install and run Netdata to visualize system and application performance metrics in real time.

## 🛠 Tools & Technologies

Netdata (Free, open-source monitoring tool)

Docker

## 🚀 Steps Performed
1. Install & Run Netdata via Docker
docker run -d \
  --name=netdata \
  -p 19999:19999 \
  --cap-add SYS_PTRACE \
  --security-opt apparmor=unconfined \
  netdata/netdata

2. Access the Netdata Dashboard

Open your browser and go to:

http://localhost:19999


Here you can monitor:

CPU usage

Memory usage

Disk I/O

Docker container stats

Network traffic

System load & performance KPIs

3. Explore Features

Charts & Panels: Visual representation of metrics

Alerts: Built-in alert system for abnormal behavior

Logs: Located at /var/log/netdata for deeper troubleshooting

## 📊 Output Screenshots

(Add screenshots of your dashboard and running metrics here.)

## ❓ Interview Questions & Answers

1. What does Netdata monitor?

CPU, memory, disk, network, Docker containers, applications, and more in real-time.

2. How to view real-time metrics?

Through the browser-based dashboard at http://localhost:19999.

3. How is Netdata different from Prometheus?

Netdata is lightweight and real-time, Prometheus is more suited for long-term storage and complex queries.

4. What is a collector?

A module in Netdata that gathers specific types of metrics (e.g., CPU, MySQL, Docker).

5. Key Performance Indicators (KPIs) to watch:

CPU load

Memory usage

Disk utilization

Network throughput

Container resource usage

6. How to deploy Netdata on a VM?

Install Docker on the VM, then run the Netdata container as shown above.

7. How does Netdata alerting work?

Preconfigured alarms trigger based on defined thresholds; notifications can be sent via email, Slack, etc.

8. What is a dashboard in this context?

The visual interface displaying all system performance charts and metrics in real time.

📂 Repository Structure
📁 task7-netdata
│── README.md
│── screenshots/
│    ├── dashboard.png
│    ├── cpu-memory.png
└── docker-run-command.txt

## 📌 Outcome

Successfully monitored a system using Netdata in Docker, explored alerts, visualized metrics, and understood real-time performance monitoring.
