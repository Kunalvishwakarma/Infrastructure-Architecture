# Synthetic Infrastructure Capacity Planning Example

> Fictional teaching example only. Values are illustrative and must not be used as production sizing recommendations.

## Objective

Demonstrate a repeatable method for assessing current utilization, forecasting demand, identifying constraints and recording assumptions.

## Example workload profile

| Metric | Current baseline | Planning assumption |
|---|---:|---:|
| vCPU allocated | 240 | 15% annual growth |
| Average CPU utilization | 52% | Peak planning target 70% |
| Memory allocated | 1,024 GB | 12% annual growth |
| Average memory utilization | 61% | Maintain operational headroom |
| Storage consumed | 18 TB | 20% annual growth |
| Storage usable capacity | 30 TB | Alert at 75% consumed |
| Network peak throughput | 1.8 Gbps | 15% annual growth |

All values are invented to illustrate the method.

## Forecast method

For a simple compound annual growth assumption:

`Future demand = Current demand × (1 + growth rate)^years`

For example, using 15% annual growth over two years:

`240 vCPU × 1.15² ≈ 317 vCPU`

This is a demand forecast, not a purchase recommendation. Apply workload-specific peak, redundancy, failure-domain and licensing requirements.

## Capacity review steps

1. Confirm measurement period and data quality.
2. Separate allocated capacity from observed consumption.
3. Review average, peak and percentile utilization.
4. Identify seasonal patterns and planned business changes.
5. Model normal operation and failure scenarios.
6. Include N+1 or other resilience requirements where applicable.
7. Check licensing, storage performance, network and power/cooling constraints.
8. Record assumptions, owners, confidence and decision dates.

## Decision record

| Question | Decision / evidence |
|---|---|
| What is the forecast horizon? | Define with service owner |
| What growth assumption is used? | Business-approved forecast |
| What headroom is required? | Based on service criticality and failure model |
| What constraints exist? | Compute, memory, storage, IOPS, network, power, licensing |
| What action is recommended? | Optimize, scale, migrate, procure or defer |
| When is the model reviewed? | Monthly / quarterly / material change |

## Caveats

Do not size production platforms from averages alone. Validate with workload owners, vendor guidance, performance testing and resilience requirements.
