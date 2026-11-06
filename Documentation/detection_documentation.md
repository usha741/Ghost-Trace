Ghost Trace – Detection Documentation
Detection Rule: Brute Force Login Attempts
Purpose

Identify repeated failed authentication attempts from a single source IP address targeting the same username.

Detection Query
spl
index=main sourcetype=csv
| eval _time=strptime(timestamp,"%Y-%m-%d %H:%M:%S")
| where status="failed"
| bin _time span=5m
| stats count by _time src_ip username
| where count >= 5
| table _time src_ip username count

Detection Logic
Retrieve authentication events from the main index.
Convert the timestamp field into Splunk time.
Filter failed authentication events.
Group events into five-minute windows.
Count attempts by source IP and username.
Display events where the count is five or higher.
Expected Output
Source IP	Username	Attempts
192.168.1.10	admin	5
Security Response
Investigate the suspicious source IP.
Review authentication history.
Check for successful logins after failed attempts.
Escalate confirmed suspicious activity.
False Positive Considerations

Legitimate users may accidentally enter incorrect passwords multiple times. Detection results must be investigated before classifying an event as malicious.

Detection Status

Threshold-based detection using simulated authentication data.
