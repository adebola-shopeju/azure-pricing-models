# LAB 15 — Azure Pricing Models

## Overview
This lab demonstrates how to estimate cloud infrastructure 
costs using the Azure Pricing Calculator for a 3-tier 
web application.

## Architecture
- Load Balancer (traffic distribution)
- 2x Virtual Machines D2 v3 (web servers - Linux)
- Azure Cache for Redis (performance caching)
- Azure SQL Database (data storage - DTU Basic)
- Blob Storage (file storage - LRS)

## Cost Summary
| Pricing Model | Monthly Cost |
|---|---|
| Pay-As-You-Go | $182.96 |
| After Optimisation | $139.51 |
| Annual Saving | $521.40 |

## Key Learnings
- Reserved Instances save ~31% vs Pay-As-You-Go
- Linux VMs are ~50% cheaper than Windows VMs
- DTU model is cheaper than vCore for small databases
- LRS is more cost effective than GRS for dev environments
- PaaS reduces management overhead vs IaaS
- Azure Hybrid Benefit saves ~50% on Windows licences

## Screenshots
14 screenshots documenting each configuration step
are included in this repository.

## Tools Used
- Azure Pricing Calculator
- Microsoft Excel
- GitHub
