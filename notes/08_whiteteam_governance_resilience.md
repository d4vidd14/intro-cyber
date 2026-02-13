# White Team Concepts (Governance, Risk & Resilience)

## CIA Triad
- **Confidentiality**: only authorized access to data.
- **Integrity**: data is accurate and not tampered with.
- **Availability**: systems/data are accessible when needed.

## Vulnerability, Risk, Impact
- **Vulnerability**: weakness that can be exploited.
- **Risk**: likelihood × impact (simplified).
- **Impact**: business damage if an event happens (financial, reputational, legal, operational).

## Governance, Resilience, Contingency
- **Governance**: policies, roles, responsibilities, and decision-making to manage security.
- **Resilience**: ability to resist, absorb, and recover from incidents.
- **Contingency**: planned actions to keep critical services running during disruptions.

## GAP analysis
- Compares “current state” vs “target state” to identify gaps and remediation actions (people/process/technology).

## Business Continuity & Disaster Recovery
- **BCP (Business Continuity Plan)**: how the business keeps operating during disruption.
- **DRP (Disaster Recovery Plan)**: how IT/services are restored after an outage.

### Key metrics
- **RTO (Recovery Time Objective)**: maximum acceptable downtime (time to restore).
- **RPO (Recovery Point Objective)**: maximum acceptable data loss measured in time (how far back you can lose data).

## KPIs / KRIs / ROE
- **KPI (Key Performance Indicator)**: measures performance (e.g., % patches applied within SLA).
- **KRI (Key Risk Indicator)**: measures risk exposure (e.g., # critical vulnerabilities open >30 days).
- **ROE (Rules of Engagement)**: agreed scope/rules for an exercise (especially for Red Team / simulations).

## Exercises & reviews
- **Injects**: simulated events/messages introduced during an exercise to drive actions/decisions.
- **MSEL (Master Scenario Events List)**: timeline/list of injects and expected play during an exercise.
- **AAR (After Action Review)**: post-exercise review: what happened, what worked, what didn’t, improvements.

## Incident response planning
- **IRP (Incident Response Plan)**: how to detect, respond, communicate, and recover from security incidents.

## Additional plans (as used in some frameworks)
*(Names can vary by organization; included as referenced in training.)*
- **CIRP (Cyber Incident Response Plan)**: cyber-specific incident response plan.
- **CMP**: crisis/communications management plan (often focused on stakeholders and messaging).
- **OEP**: operational/emergency plan (continuity actions during disruption).

## Practical takeaway
- White Team focuses on aligning security with business objectives through governance, risk management, and resilience planning.
- Exercises (MSEL/injects) + AAR help validate plans (BCP/DRP/IRP) and improve them continuously.
