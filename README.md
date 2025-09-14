# 🛡️ Threat-Aware Infrastructure as Code Linter

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Status](https://img.shields.io/badge/status-experimental-orange)]()
[![CI/CD](https://img.shields.io/badge/CI%2FCD-ready-blue)]()

**Stop security incidents before they happen.**  
Proactively scan your Terraform, CloudFormation, and Kubernetes configs against **real-time threat intelligence feeds** — directly in your CI/CD pipeline.

---

## 🚨 Why This Matters

Security and DevOps teams operate in silos:

- DevOps builds with **IaC** (Terraform, CloudFormation, Kubernetes)  
- Threat Intel teams track **malicious IPs & domains**  
- The gap? Risky configs slip into production — like firewall rules allowing `0.0.0.0/0` that overlap with **known C2 servers**  

👉 Result: Issues discovered **after deployment**, when it’s too late.

---

## ✅ The Solution

This tool **shifts security left** by embedding live threat intelligence into your pipeline.

```text
⚠️ Threat-Aware IaC Findings:
- Resource `web-server` allows ingress traffic to CIDR 0.0.0.0/0 which overlaps IOC 203.0.113.10/32
- Resource `web-server` allows egress traffic to CIDR 0.0.0.0/0 which overlaps IOC 45.67.89.0/24

❌ Blocking deployment due to security risks
