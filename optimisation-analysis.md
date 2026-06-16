# Optimisation Analysis

## 1. Pay-As-You-Go vs Reserved Instances

| Pricing Model | Monthly Cost |
|---|---|
| Pay-As-You-Go | $182.96 |
| 1 Year Reserved | $139.51 |
| Monthly Saving | $43.45 |
| Annual Saving | $521.40 |

Switching both VMs from Pay-As-You-Go to a 1 year 
savings plan reduced costs by approximately 31%. 
This is ideal for workloads that run consistently 
24/7 and do not need flexibility.

## 2. LRS vs GRS Backup Redundancy

| Redundancy | Protection | Cost Impact |
|---|---|---|
| LRS | Same region only | Lower cost |
| GRS | Two regions | Higher cost |
| RA-GRS | Two regions + readable | Highest cost |

LRS was selected for this lab as it is the most 
cost effective option for development environments. 
Production systems handling critical data should 
consider GRS or RA-GRS for disaster recovery.

## 3. IaaS vs PaaS

| Model | Example | Management | Cost |
|---|---|---|---|
| IaaS | Virtual Machines | Self managed | Higher overhead |
| PaaS | Azure App Service | Microsoft managed | Lower overhead |

For a small startup, PaaS is recommended because 
Microsoft manages the underlying infrastructure, 
removing the need for a dedicated system administrator. 
This reduces both technical overhead and staffing costs.

## 4. Azure Hybrid Benefit

Companies with existing Windows Server licences can 
apply Azure Hybrid Benefit to reduce VM costs by 
approximately 50%. Linux VMs do not require this 
as Linux is free by default.


## 5. Spot VMs vs Reserved Instances vs Pay-As-You-Go

| Pricing Model | Discount | Interruption Risk | Best For |
|---|---|---|---|
| Pay-As-You-Go | 0% | None | Unpredictable workloads |
| 1 Year Reserved | ~31% | None | Steady 24/7 workloads |
| 3 Year Reserved | ~53% | None | Long term stable workloads |
| Spot VMs | up to 90% | High (30 sec notice) | Interruptible batch jobs |

### When to Use Spot VMs
Spot VMs are ideal for workloads that can be interrupted 
and restarted without data loss. Examples include:
- Video encoding and rendering
- Big data analytics and processing
- Development and testing environments
- Machine learning model training

### When NOT to Use Spot VMs
Spot VMs are NOT suitable for:
- Web servers serving live customer traffic
- Production databases
- Any application requiring continuous availability

### Break-Even Analysis: 1 Year vs 3 Year Savings Plan

| Plan | Monthly Cost (per VM) | Annual Cost | Total over 3 years |
|---|---|---|---|
| Pay-As-You-Go | $70.08 | $840.96 | $2,522.88 |
| 1 Year Reserved | ~$48.36 | $580.32 | $1,740.96 |
| 3 Year Reserved | ~$32.94 | $395.28 | $1,185.84 |

The 3 year plan saves $555.12 more than the 1 year plan 
over 3 years. The break-even point is immediate — the 
3 year plan is cheaper from month one. However it 
requires a longer commitment, which carries risk if 
business needs change.

Recommendation: Choose 1 year Reserved for flexibility 
or 3 year Reserved only if the workload is guaranteed 
to run for 3+ years.

## Conclusion
Through optimisation, monthly costs were reduced 
from $182.96 to $139.51 — a saving of $43.45 per 
month or $521.40 per year.
