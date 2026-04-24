# 01 — Performance Monitoring

## Sources

| Source | Reference |
|--------|-----------|
| ETA Framework | Point 7: Build something future-proof (continuous monitoring) |
| Service Standard | Point 10: Define what success looks like and publish performance data |
| Service Standard | Point 8: Iterate and improve frequently |
| AI Playbook | Principle 5: Managing the full AI lifecycle |
| Turing Institute FAST | Sustainability: maintaining accuracy, reliability over time |

## Purpose

Evaluation is not a one-time event. The ETA Framework requires continuous monitoring with formal review points at minimum quarterly. The Service Standard requires publishing performance data. The AI Playbook requires monitoring for drift, bias, and hallucinations.

## Monitoring Requirements

### Key performance indicators

| KPI | Description | Frequency | Source |
|-----|-------------|-----------|--------|
| Accuracy rate | % factually correct responses | Weekly | SS Point 10 |
| Hallucination rate | % responses with fabricated content | Weekly | AIP Principle 1 |
| User satisfaction | User feedback scores | Monthly | SS Point 1 |
| Task completion rate | % of user goals successfully met | Weekly | SS Point 10 |
| Response time | Average and p95 latency | Daily | SS Point 14 |
| Error rate | % failed requests | Daily | SS Point 14 |
| Escalation rate | % of interactions requiring human intervention | Weekly | AIP Principle 4 |
| Complaint rate | Complaints related to AI outputs | Monthly | WP Principle 5 |

### Model drift detection

- [ ] Baseline performance metrics recorded at deployment
- [ ] Automated alerts when metrics deviate from baseline beyond threshold
- [ ] Regular comparison of current vs. baseline performance
- [ ] Investigation triggered when drift is detected

### User feedback

- [ ] Feedback mechanism built into the service
- [ ] Feedback is analysed regularly
- [ ] Patterns in negative feedback trigger investigation
- [ ] User research conducted periodically (not just at launch)

### Publishing performance data (SS Point 10)

- [ ] Performance dashboard created
- [ ] Data published at agreed cadence
- [ ] Data is accessible and understandable to non-technical audiences

## Output

1. Monitoring dashboard specification
2. Alert threshold definitions
3. Performance reporting schedule
4. Published performance data
