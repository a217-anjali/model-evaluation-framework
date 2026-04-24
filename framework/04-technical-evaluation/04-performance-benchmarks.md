# 04 — Performance Benchmarks

## Sources

| Source | Reference |
|--------|-----------|
| AISI Evaluations | Automated Capability Assessments |
| CDEI AI Assurance Portfolio | Performance Testing |
| Service Standard | Point 10: Define what success looks like and publish performance data |

## Purpose

Establish quantitative benchmarks for the LLM's performance in the target domain. AISI uses automated capability assessments as "broad but shallow tools providing baseline performance indications." The Service Standard (Point 10) requires defining success and publishing performance data.

## Benchmark Categories

### Task performance

- [ ] Define the core tasks the LLM must perform
- [ ] Create a test dataset for each task (minimum statistically significant sample)
- [ ] Measure task completion rate
- [ ] Measure task quality (human-rated or automated scoring)
- [ ] Compare against baseline (human performance or previous system)

### Response quality

| Metric | Description | How to Measure |
|--------|-------------|----------------|
| Relevance | Does the response address the question? | Human rating (1-5 scale) |
| Completeness | Does it cover all necessary information? | Human rating against checklist |
| Accuracy | Is the information factually correct? | Domain expert verification |
| Clarity | Is the response understandable? | Readability scoring + user testing |
| Consistency | Same question, same quality answer? | Repeat testing |

### Latency and reliability

- [ ] Average response time measured
- [ ] 95th percentile response time measured
- [ ] Error rate (failed requests, timeouts)
- [ ] Throughput capacity under expected load
- [ ] Performance under peak load

### Comparative evaluation

- [ ] Benchmark against alternative models (if applicable)
- [ ] Benchmark against the current non-AI process
- [ ] Cost-per-query comparison across alternatives

## Publishing Performance Data (SS Point 10)

- [ ] Performance metrics defined and agreed
- [ ] Baseline measurements recorded
- [ ] Targets set for each metric
- [ ] Reporting cadence established (link to Section 08)
- [ ] Performance data published (where appropriate)

## Output

1. Benchmark test results
2. Performance metrics dashboard specification
3. Defined thresholds for acceptable vs. unacceptable performance
