## Firewall Design

HTTP Rule
- Port: 80
- Source: 0.0.0.0/0

SSH Rule
- Port: 22
- Source: User public IP only
- Target: VM service account

This ensures least-privilege network access.