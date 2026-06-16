# Architecture Summary

## Region
East US

## Services & Assumptions

| Service | Configuration | Assumption |
|---|---|---|
| Load Balancer | Basic Tier | Low traffic volume |
| VM 1 | D2 v3, 2 vCPU, 8GB RAM, Linux | 730 hours/month |
| VM 2 | D2 v3, 2 vCPU, 8GB RAM, Linux | 730 hours/month |
| Redis Cache | Basic C0, 250MB | 730 hours/month |
| SQL Database | DTU Basic, 5 DTUs, 2GB | 730 hours/month |
| Blob Storage | Standard, LRS, Hot tier | 1000 GB/month |

## Usage Patterns
- Both VMs run 24/7 (730 hours per month)
- Outbound bandwidth estimated at 100GB/month
- Single database instance for development workload
- Blob storage used for static files and backups
