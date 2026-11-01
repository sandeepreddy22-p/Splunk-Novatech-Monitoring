# Troubleshooting Common Issues

# 1. Data Not Appearing in Search
* Cause: Incorrect sourcetype or firewall blocking port 9997.
* Resolution: Checked `splunkd.log` for connection errors and verified AWS security group rules.

## 2. Forwarder Connection Timeout
* Cause: Target standalone instance IP or port misconfigured in `outputs.conf`.
* Resolution: Tested network connectivity using `telnet <splunk-server-ip> 9997`.

## 3. High CPU / Disk Usage
* Cause: Excessive debug-level logging or unparsed log streams.
* Resolution: Filtered unnecessary logs using custom `props.conf` and `transforms.conf` rules.
