# Splunk-Based Security Monitoring Environment for Threat Detection and Analysis

## Overview
This project focuses on designing a comprehensive security monitoring environment using Splunk for a fictional organization. The environment was tested against simulated attacks and includes a detailed analysis of both Windows Server and Apache Web Server logs. The goal is to identify, analyze, and respond to potential security threats by detecting suspicious patterns in log data.

## Tools & Technologies
- **Splunk:** Central platform for log ingestion, monitoring, and analysis.
- **Windows Server Logs:** Analyzed to detect suspicious changes in severity, failed activities, successful logins, and account deletions.
- **Apache Web Server Logs:** Monitored for HTTP method usage, response codes, and international activity.

## Key Findings

### Suspicious Activity in Windows Logs
- **Severity Escalation:** Incident severity increased from 329 to 1111 events.
- **Failed Login Alerts:** A spike in failed logins on 3/25/2020 prompted an adjustment in alert thresholds.
- **Successful Logins:** Unusual login activity, notably by "User_j" with a peak of 194 logins within an hour.

### Web Server Log Analysis
- **HTTP POST Anomalies:** A surge in POST requests from 106 to 1324 events suggests possible data exfiltration or exploitation attempts.
- **International Activity:** A significant volume of activity from Ukraine, with a cluster originating from Kyiv (440 events).
- **Suspicious URIs:** Repeated access to the URI 'VSI_Account_Logon.php' indicating potential credential harvesting or brute-force attempts.

## Alert & Dashboard Configurations
- **Custom Alert Thresholds:** Fine-tuned to balance sensitivity while reducing false positives.
- **Dashboards:** Developed with time charts, cluster maps, and statistical visualizations to highlight suspicious patterns in user behavior and HTTP methods.

## Analytical Insights
- **User Behavior Analysis:** Correlated anomalous activity (e.g., from "User_a" and "User_k") with login attempts and account lockouts.
- **Signature Analysis:** Noted high occurrences of events like "Account locked out" and "Password reset attempts" during key time windows.
- **Dynamic Reporting:** Evaluated the benefits and trade-offs of various visualization techniques (bar graphs, pie charts, statistical reports) to best represent the data.

## Challenges & Adjustments
- **Alert Threshold Fine-Tuning:** Critical due to large spikes in activity during simulated attacks.
- **Cross-Referencing Log Sources:** Emphasized the importance of correlating multiple log sources and visualization methods for a comprehensive threat analysis.

## Detailed Presentation
For a more comprehensive walkthrough of the monitoring environment and analytical findings, please refer to the detailed presentation:
- **[View the Detailed Presentation PDF](./CHET%20FLOWERS_Splunk-Based-Security-Monitoring-Environment-for-Threat-Detection-and-Analysis.pdf)**
  *(Ensure that the PDF file in your repository matches this filename exactly.)*

## Conclusion
This project demonstrates a robust approach to real-time threat detection and analysis using Splunk. By integrating log data from both Windows and Apache servers, the environment provides actionable insights into suspicious activities. The project underscores the importance of tailored alert configurations and dynamic dashboards to enhance an organization’s security posture.
