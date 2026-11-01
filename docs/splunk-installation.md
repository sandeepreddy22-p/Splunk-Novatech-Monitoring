# Splunk Enterprise Installation

## Installation Procedure on Linux (EC2)
1. Downloaded the Splunk Enterprise Linux tarball package onto the EC2 instance.
2. Extracted the package into `/opt/splunk`:
   ```COMMAND PROMPT
   tar -xvzf splunk-<version>-Linux-x86_64.tgz -C /opt/
 /opt/splunk/bin/splunk start --accept-license
/opt/splunk/bin/splunk enable boot-start -user splunk
  
Verified the Splunk Web service is running by accessing http://<ec2-public-ip>:8000 in the browser.
