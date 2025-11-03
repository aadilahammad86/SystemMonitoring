# Directory Overview

This directory contains documentation and configuration files for a system monitoring stack. The setup uses Prometheus for metrics collection, Grafana for visualization, and Headscale/Tailscale for secure networking. The monitoring is set up on a GCP VM and targets remote Windows servers.

## Key Files

*   `Setup_for_Grafana_Monitoring_with _Prometheus_(Ubuntu_GCP).md`: Instructions for setting up Grafana and Prometheus on an Ubuntu server in Google Cloud Platform.
*   `Setup_for_Windows_Exporter_Windows_Servers.md`: Instructions for installing and configuring the `windows_exporter` on remote Windows servers to collect metrics.
*   `Remote Configuration on the Prometheus Server (GCP VM).md`: Guide for configuring the central Prometheus server to scrape metrics from the remote Windows hosts.
*   `Setup_for_Headscale_and_Tailscale.md`: Instructions for setting up a secure, private network using Headscale (a self-hosted Tailscale control server) and Tailscale clients. This allows Prometheus to scrape metrics over an encrypted overlay network instead of the public internet.
*   `*.json`: These files are likely Grafana dashboard configurations that can be imported to visualize the collected metrics.
    *   `Microsoft_SQL_Server_Dashboard.json`
    *   `Running_Web_Apps.json`
    *   `Windows_Dashboard.json`
    *   `windows_server_dashboard.json`

## Usage

This directory serves as a knowledge base and configuration store for the monitoring infrastructure. The markdown files provide step-by-step instructions for setting up and maintaining the system. The JSON files can be imported into Grafana to quickly create dashboards.

To use this repository:

1.  **Set up the central monitoring server:** Follow the instructions in `Setup_for_Grafana_Monitoring_with _Prometheus_(Ubuntu_GCP).md`.
2.  **Set up monitoring on target machines:** Follow `Setup_for_Windows_Exporter_Windows_Servers.md` for each Windows server you want to monitor.
3.  **Configure Prometheus to scrape targets:** Use `Remote Configuration on the Prometheus Server (GCP VM).md` to add the Windows servers to the Prometheus scrape list.
4.  **(Recommended)** **Secure the connection:** Follow `Setup_for_Headscale_and_Tailscale.md` to secure the communication between the Prometheus server and the exporters.
5.  **Visualize the data:** Import the `.json` files into your Grafana instance to create pre-configured dashboards.
