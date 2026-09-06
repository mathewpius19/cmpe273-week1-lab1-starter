# CMPE 273 – Week 1 Lab 1: Your First Distributed System (Starter)

This starter provides two implementation tracks:
- `python-http/` (Flask + requests)
- `go-http/` (net/http)

Pick **one** track for Week 1.

## Lab Goal
Build **two services** that communicate over the network:
- **Service A** (port 8080): `/health`, `/echo?msg=...`
- **Service B** (port 8081): `/health`, `/call-echo?msg=...` calls Service A

Minimum requirements:
- Two independent processes
- HTTP (or gRPC if you choose stretch)
- Basic logging per request (service name, endpoint, status, latency)
- Timeout handling in Service B
- Demonstrate independent failure (stop A; B returns 503 and logs error)

## Success/Failure Screenshot:

<img width="682" height="166" alt="2026-09-06_12-48-34" src="https://github.com/user-attachments/assets/c951610d-6e84-41be-9714-651cb8b34e09" />

## Why is this system distributed?
This system is distributed because there are two separate processes trying to communicate over a network. Since they both run as two independent processes, any network or service downtime can cause the communication to fail as shown in the screenshot.
