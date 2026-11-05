# Ghost-Trace
Splunk-Based Brute Force Attack Detection and Authentication Monitoring

👻 GHOST TRACE

Automated Brute-Force Attack Detection Using Splunk

Project Overview

Ghost Trace is a cybersecurity monitoring project developed using Splunk to detect multiple failed login attempts and potential brute-force attacks.

The system analyzes authentication logs, identifies suspicious IP addresses, monitors targeted usernames and generates security alerts based on predefined detection rules.

Project Objectives

- Detect repeated failed login attempts.
- Identify suspicious source IP addresses.
- Monitor targeted user accounts.
- Detect potential brute-force attacks.
- Correlate failed and successful login activities.
- Generate security alerts.

Technologies Used

- Splunk
- SPL (Search Processing Language)
- CSV Authentication Logs
- GitHub

Key Features

1. Failed Login Monitoring
2. Brute-Force Attack Detection
3. Suspicious IP Identification
4. Username Monitoring
5. Login Event Correlation
6. Security Alert Generation
7. SOC Monitoring Dashboard

Detection Logic

The system identifies five or more failed login attempts from the same source IP and username within a five-minute time bucket.

Project Architecture

Authentication Logs → Splunk → SPL Detection Rules → Security Alerts → SOC Dashboard

Project Structure

- Sample-Logs
- Splunk-Queries
- Dashboards
- Alerts
- Documentation
- Screenshots

Testing

The project uses simulated authentication logs to validate detection rules.

Limitations

This project uses simulated data and threshold-based detection. Security alerts require analyst investigation.

Author

USHA C

Project Category

SOC Analyst | SIEM | Threat Detection | Splunk

Disclaimer

Developed for educational and defensive cybersecurity purposes.