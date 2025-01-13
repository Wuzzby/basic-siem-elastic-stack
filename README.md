# Basic SIEM with Elastic Stack

## Overview
This project demonstrates how to build a basic Security Information and Event Management (SIEM) system using the Elastic Stack. It centralizes logs from a Linux server and a Windows VM, enabling real-time monitoring, visualization, and alerting.

System Architecture:

## Tools and Technologies
- **Elastic Stack**:
  - Elasticsearch 8.17.0
  - Kibana 8.17.0
  - Filebeat 8.17.0
  - Winlogbeat 8.17.0
- **Operating Systems**:
  - Ubuntu Server 20.04
  - Windows 10
- **Virtualization**:
  - VirtualBox

## Steps to Reproduce
### 1. Set Up Elasticsearch and Kibana
- Install Elasticsearch on Ubuntu Server:
  ```bash
  sudo apt install elasticsearch

- Configure elasticsearch.yml for single-node mode:
     discovery.type: single-node

- Install Kiabana and verify:
     curl -X GET "http://127.0.0.1:9200"

2. Configure Filebeat
	Install Filebeat on Ubuntu Server.
	Configure filebeat.yml (see filebeat.yml).


3. Configure Winlogbeat
	Install Winlogbeat on Windows VM.
	Configure winlogbeat.yml (see winlogbeat.yml).


4. Visualize Logs in Kibana
	Build visualizations and dashboards.

## Challenges and Solutions:

Elasticsearch Failing to Start:
	Fixed by setting discovery.type: single-node in elasticsearch.yml.

Empty Replies from Elasticsearch:
	Resolved by changing network.host to 0.0.0.0.

## Results
	Centralized logging from Linux and Windows.
	Real-time monitoring using Kibana dashboards.

## Medium Write-Up
For a detailed walkthrough, visit my Medium article:
[Building a Basic SIEM with the Elastic Stack](https://medium.com/@SamAchek/building-a-basic-siem-with-the-elastic-stack-a-step-by-setp-guide-06840fe09aa7)


## License 
	This project is licensed under the MIT License

