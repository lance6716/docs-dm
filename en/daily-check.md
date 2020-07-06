---
title: Daily Check
summary: Learn about the daily check of TiDB Data Migration (DM).
category: reference
---

# Daily Check

This document summarizes how to perform a daily check on TiDB Data Migration (DM).

+ Method 1: Execute the `query-status` command to check the running status of the task and the error output (if any). For details, see [Query Status](query-status.md).

+ Method 2: If Prometheus and Grafana are correctly deployed when you deploy the DM cluster using DM-Ansible, you can view DM monitoring metrics in Grafana. For example, suppose that the Grafana's address is `172.16.10.71`, go to <http://172.16.10.71:3000>, enter the Grafana dashboard, and select the DM Dashboard to check monitoring metrics of DM. For more information of these metrics, see [DM Monitoring Metrics](monitor-a-dm-cluster.md).

+ Method 3: Check the running status of DM and the error (if any) using the log file.

    - DM-master log directory: It is specified by the `--log-file` DM-master process parameter. If DM is deployed using DM-Ansible, the log directory is `{ansible deploy}/log/dm-master.log` in the DM-master node.
    - DM-worker log directory: It is specified by the `--log-file` DM-worker process parameter. If DM is deployed using DM-Ansible, the log directory is `{ansible deploy}/log/dm-worker.log` in the DM-worker node.