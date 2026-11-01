# Splunk Universal Forwarder Installation

# Overview
Installed and configured the Splunk Universal Forwarder agent on remote target endpoints (Linux and Windows servers) to collect and forward telemetry data securely.

# Installation & Configuration Steps
1. Downloaded the Splunk Universal Forwarder package corresponding to the target OS.
2. Installed and registered the forwarder service, pointing it to the designated Indexer / Heavy Forwarder listening on port `9997`.
3. Configured `outputs.conf` to establish secure communication:
   ```ini
   [tcpout]
   defaultGroup = default-autolb-group

   [tcpout:default-autolb-group]
   server = <indexer-ip>:9997

   Validated active forwarding connections using the CLI status check:
         ./splunk list forward-server
