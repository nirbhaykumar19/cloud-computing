# GCP VM Auto-Scaling, Monitoring & Security Setup

## Objective
To demonstrate VM autoscaling in Google Cloud using CPU metrics,
with secure IAM configuration, centralized monitoring, logging,
and strict cost control.

## Architecture Overview
- Instance Template as VM blueprint
- Managed Instance Group for VM lifecycle
- Autoscaler based on CPU utilization
- Ops Agent for monitoring and logging
- IAM separation between human users and VM identities

## Autoscaling Logic
- Minimum instances: 1
- Maximum instances: 3
- Scaling metric: CPU utilization
- Target utilization: 60%
- Alert threshold: 80%

## Security Model
- Human user access controlled by IAM roles
- VM identity managed via Service Accounts
- No static credentials stored on VM
- Authentication via Metadata Server

## Cost Control
- Budget alerts configured at 50%, 90%, 100%
- Instance Group deletion stops all charges
- Designed to operate within free credits

## Cleanup
Delete the Managed Instance Group to terminate all VMs and stop billing.