# AWS EC2 Instance Setup

# Overview
Configured and provisioned multiple AWS EC2 instances (Ubuntu/Amazon Linux 2 and Windows Server) to host the distributed Splunk enterprise environment for NovaTech Industries.

## Configuration Steps
1. Logged into the AWS Management Console and navigated to the EC2 Dashboard.
2. Launched instances with appropriate instance types (`t2.medium` / `t3.large`).
3. Configured **Security Groups** to allow inbound traffic on required ports:
   * `8000` (Splunk Web UI)
   * `8089` (Splunk Management)
   * `9997` (Splunk S2S Forwarding)
   * `22` (SSH) / `3389` (RDP)
