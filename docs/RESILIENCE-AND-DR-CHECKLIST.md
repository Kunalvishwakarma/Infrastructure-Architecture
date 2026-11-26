# Resilience and Disaster Recovery Design Checklist

> A planning aid, not a substitute for business impact analysis, approved recovery plans or tested procedures.

## Requirements
- [ ] Business impact analysis identifies critical services and dependencies.
- [ ] Service owners approve recovery time objective (RTO) and recovery point objective (RPO).
- [ ] Availability requirements and maintenance windows are documented.
- [ ] Data classification, retention and regulatory constraints are understood.

## Architecture
- [ ] Failure domains are identified: component, rack, site, carrier, region and identity.
- [ ] Critical dependencies do not introduce unrecognized single points of failure.
- [ ] Backup copies are protected against deletion, ransomware and unauthorized access.
- [ ] Replication consistency and failover behavior are understood.
- [ ] DNS, identity, certificates, secrets and network paths are included in recovery design.
- [ ] Capacity is sufficient for the recovery scenario.

## Operations
- [ ] Recovery roles, authority and communications are defined.
- [ ] Runbooks are version-controlled and access-controlled.
- [ ] Monitoring detects loss of replication, backup failure and service degradation.
- [ ] Suppliers and third-party dependencies are included in exercises.

## Testing
- [ ] Backup restore tests completed and evidence retained.
- [ ] Recovery exercises test business transactions, not only infrastructure startup.
- [ ] Failback and data reconciliation are considered.
- [ ] Findings have owners, due dates and tracked closure.
- [ ] RTO/RPO achievement is measured from test evidence, not assumed from design.

## Reporting
Record test date, scope, scenario, actual recovery times, data-loss window, defects, business acceptance and improvement actions.
