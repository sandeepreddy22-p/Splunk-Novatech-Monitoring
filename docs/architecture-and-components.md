# Splunk Architecture & Component Connection

# Architecture Design (Standalone Environment)
  # Splunk Enterprise Standalone Instance:** Deployed on a single AWS EC2 instance combining all core Splunk capabilities into one unified server:
  * Search Head : Handles user queries, custom dashboard creation, and alert rules.
  * Indexers : Stores parsed log data locally in indexed buckets and handles search execution.
  * Receivers: Listens for incoming data streams from Universal Forwarders.
  * Universal Forwarders:Installed on remote target endpoints (Linux/Windows servers) to collect raw logs locally and securely forward them to the standalone Splunk instance.

## Component Connection
* Configured `outputs.conf` on Universal Forwarders to establish secure data streams pointing directly to the standalone Splunk instance IP on port `9997`.
* Configured `inputs.conf` on the standalone Splunk receiver to accept incoming forwarding data streams.
