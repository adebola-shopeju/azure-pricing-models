# Regional Pricing Analysis

## Overview
Azure pricing varies by region due to differences in 
electricity costs, land costs, and local taxes.
This analysis compares the same 3-tier architecture 
across three global regions.

## Regional Cost Comparison

| Service | East US | West Europe | Southeast Asia |
|---|---|---|---|
| Load Balancer | $0.00 | $0.00 | $0.00 |
| VM 1 (D2 v3 Linux) | $70.08 | $78.84 | $82.16 |
| VM 2 (D2 v3 Linux) | $70.08 | $78.84 | $82.16 |
| Redis Cache (C0) | $16.06 | $17.52 | $18.25 |
| SQL Database (Basic) | $4.90 | $5.15 | $5.25 |
| Blob Storage (LRS) | $21.84 | $23.47 | $25.12 |
| **Monthly Total** | **$182.96** | **$203.82** | **$212.94** |
| **vs East US** | baseline | +11.4% | +16.4% |

## Key Findings

- East US is the cheapest region for this workload
- West Europe costs approximately 11.4% more than East US
- Southeast Asia costs approximately 16.4% more than East US

## Why Do Regions Have Different Prices?

1. **Energy costs** — Electricity is cheaper in some 
   US regions due to abundant power infrastructure
2. **Land and construction costs** — Data centre 
   building costs vary by country
3. **Local taxes and regulations** — Some regions 
   have higher compliance costs
4. **Currency and exchange rates** — Prices reflect 
   local market conditions

## Data Egress Costs by Region

Data egress (outbound transfer) is charged when data 
leaves an Azure data centre to the internet.

| Region | First 100GB/month | Next 9.9TB/month |
|---|---|---|
| East US | Free | $0.087/GB |
| West Europe | Free | $0.087/GB |
| Southeast Asia | Free | $0.096/GB |

### Egress Cost Example — 100GB Outbound Per Month

| Region | Egress Cost |
|---|---|
| East US | $0.00 (within free tier) |
| West Europe | $0.00 (within free tier) |
| Southeast Asia | $0.00 (within free tier) |

All three regions include 100GB free outbound transfer 
per month. Our estimated 100GB/month workload falls 
exactly within this free tier across all regions.

### Egress Cost Example — 500GB Outbound Per Month

| Region | First 100GB | Remaining 400GB | Total |
|---|---|---|---|
| East US | $0.00 | $34.80 | $34.80 |
| West Europe | $0.00 | $34.80 | $34.80 |
| Southeast Asia | $0.00 | $38.40 | $38.40 |

## Recommendation

Deploy in **East US** for this workload because:
- Lowest VM and storage costs
- Same free egress tier as other regions
- Low latency for North American users
- Largest selection of Azure services available
