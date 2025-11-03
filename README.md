# System Monitoring Configuration

This repository contains the documentation and configuration files for setting up a comprehensive system monitoring stack. The primary goal of this project is to monitor remote Windows servers using a centralized monitoring server running on a GCP VM.

## Architecture

The monitoring stack is composed of the following components:

*   **Prometheus:** For time-series data collection and storage.
*   **Grafana:** For data visualization and dashboarding.
*   **Windows Exporter:** To expose Windows system metrics to Prometheus.
*   **Headscale & Tailscale:** For creating a secure, private network for metric scraping, eliminating the need to expose monitoring endpoints to the public internet.

The central monitoring server is hosted on an Ubuntu VM in Google Cloud Platform (GCP), and the target servers are remote Windows machines.

## Getting Started

To deploy this monitoring stack, follow the setup guides in the order listed below.

1.  **[Initial Setup for Grafana Monitoring with Prometheus (Ubuntu/GCP)](Setup_for_Grafana_Monitoring_with%20_Prometheus_(Ubuntu_GCP).md)**
    *   This guide walks you through installing and configuring Grafana and Prometheus on your central monitoring server.

2.  **[Setup for Windows Exporter on Windows Servers](Setup_for_Windows_Exporter_Windows_Servers.md)**
    *   This guide explains how to install and configure the `windows_exporter` on your remote Windows machines to collect metrics.

3.  **[Remote Configuration on the Prometheus Server](Remote%20Configuration%20on%20the%20Prometheus%20Server%20(GCP%20VM).md)**
    *   This document shows how to configure your central Prometheus server to discover and scrape metrics from your remote Windows servers.

4.  **[Secure Monitoring with Headscale and Tailscale](Setup_for_Headscale_and_Tailscale.md)**
    *   **(Recommended)** This guide provides instructions for setting up a secure overlay network with Headscale and Tailscale. This is the recommended way to connect your servers, as it avoids exposing monitoring endpoints to the public internet.

## Grafana Dashboards

This repository includes pre-configured Grafana dashboards. You can import these JSON files into your Grafana instance to get started with visualizing your data quickly.

*   `Microsoft_SQL_Server_Dashboard.json`
*   `Running_Web_Apps.json`
*   `Windows_Dashboard.json`
*   `windows_server_dashboard.json`

To import a dashboard, go to the Grafana UI, navigate to "Dashboards" -> "Import", and upload the JSON file.
