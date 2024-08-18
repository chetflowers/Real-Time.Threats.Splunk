Splunk-Based-Security-Monitoring-Environment-for-Threat-Detection-and-Analysis

Overview:
This project focuses on designing a comprehensive security monitoring environment using Splunk for a fictional organization. The environment was tested against simulated attacks, followed by a detailed analysis of Windows Server and Apache Web Server logs. The goal was to identify, analyze, and respond to potential security threats based on suspicious patterns detected in log data.

Tools & Technologies:
- Splunk: Central platform for log ingestion, monitoring, and analysis.
- Windows Server Logs: Analyzed to detect suspicious changes in severity, failed activities, successful logins, and account deletions.
- Apache Web Server Logs: Monitored for HTTP method usage, response codes, and international activity.

Key Findings:
1. Suspicious Activity Detected in Windows Logs:
   - Severity Escalation: Incident severity rose from 329 to 1111 events.
   - Failed Login Alerts: Failed logins spiked on 3/25/2020, leading to an adjustment in alert thresholds.
   - Successful Logins: Unusual login activity detected, particularly from "User_j" with a peak of 194 logins within an hour.

2. Web Server Log Analysis:
   - HTTP POST Anomalies: POST requests surged from 106 to 1324 events, indicating possible data exfiltration or exploitation attempts.
   - International Activity: A large volume of activity from Ukraine, with a significant cluster originating from Kyiv (440 events).
   - Suspicious URIs: The URI 'VSI_Account_Logon.php' was repeatedly accessed, suggesting credential harvesting or brute-force attempts.

3. Alert & Dashboard Configurations:
   - Custom alert thresholds were adjusted to balance between sensitivity and minimizing false positives.
   - Dashboards included time charts, cluster maps, and statistical charts to visualize suspicious patterns, focusing on user behavior and HTTP methods.

Analytical Insights:
- User Behavior Analysis: Detected anomalous activity involving specific users ("User_a" and "User_k"), correlating with login attempts and account lockouts.
- Signature Analysis: High occurrences of events like "Account locked out" and "Password reset attempts" during critical time windows.
- Dynamic Reporting: Emphasized the advantages and trade-offs of different visualization techniques like bar graphs, pie charts, and statistical reports.

Challenges & Adjustments:
- Fine-tuning alert thresholds was critical due to large spikes in activity during simulated attacks.
- The project underscored the importance of cross-referencing different log sources and visualization methods to gain a comprehensive understanding of suspicious activities.
