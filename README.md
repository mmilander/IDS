# Network IDS

## Authors
* Maxwell Reese
* Mitchell Milander
* Blake Platt

## Preview

Similar to other independent IDS systems, this IDS consists of four main modules: packet capture, traffic analysis, threat detection, and alert generation. The application’s front-end uses Qt to display incoming packets from Npcap, similar to Wireshark. Python is extensively used for back-end processes like packet analysis, packet detection, and sending alerts. Alerts are both sent to the Qt GUI and an Elasticsearch-Kibana dashboard that displays additional metrics like CPU usage. Before the front-end and back-end were connected, the Python IDS was using the library, Scapy, to capture packets. The Scapy-related tutorial code has been left in (but commented out) incase anyone is interested in observing it. A stretch goal is to implement an SSH Honeypot to attract malicious traffic as well as display more packet information, such as payload data, on the Qt GUI.

## Installation

* Python 3.10+
* Npcap installed
* Npcap SDK

## Prerequisites
* Qt
* Docker

### Steps to Run
- Start Docker
- cd into the folder 'IDS Deployable' 
- Start run_ids.bat which will show in the terminal and open an Elastic metrics dashboard
- Then from 'IDS Deployable', cd into Qt_IDS_Interface and run the Qt Project file

## Known Problems

- Requires administrative privileges
- High traffic volumes may impact performance
- Detection is currently rule-based (limited ML integration)
- Windows-dependent due to Npcap
- Issues connecting to Kibana -- most issues currently get solved by either reloading the page or restarting the bat file after closing everything
- Issues connecting with Elastic/Docker -- if these arise (mostly after running and closing) delete the Docker container and then run the bat file again

## Additional Documentation
* [Sprint Report 1](https://github.com/mmilander/IDS/blob/main/CPT_S%20322%20Class%20Assignments/Sprint_1/SPRINT_REPORT_1.md)
* [Sprint Report 2](https://github.com/mmilander/IDS/blob/main/CPT_S%20322%20Class%20Assignments/Sprint_2/Sprint%202%20Report.md)
* [Sprint Report 3](https://github.com/mmilander/IDS/blob/main/CPT_S%20322%20Class%20Assignments/Sprint_3/Sprint_3_report.md)
* [Final Report](https://github.com/mmilander/IDS/blob/main/CPT_S%20322%20Class%20Assignments/FinalReport.pdf)
* [Sources](https://github.com/mmilander/IDS/blob/main/Sources.md)
* [License](https://github.com/mmilander/IDS/blob/main/LICENSE.txt)

## Screenshots of Final Prototype
### Qt Interface
![Qt Interface](https://github.com/mmilander/IDS/blob/main/Tests%20%26%20Research/FinalPrototypeScreenshot/Qt%20Interface.png)

### Elastic Dashboard
![Kibana Dashboard](https://github.com/mmilander/IDS/blob/main/Tests%20%26%20Research/FinalPrototypeScreenshot/Elastic%20Dashboard.png)

