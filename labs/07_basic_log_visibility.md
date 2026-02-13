# Lab: Basic log visibility (Ubuntu)

## Authentication logs (SSH/login activity)
sudo tail -n 50 /var/log/auth.log

## System logs (if available)
sudo journalctl -n 50

Goal:
- Identify failed logins, successful logins, and timestamps.
- Think: what could become an IOC here?
