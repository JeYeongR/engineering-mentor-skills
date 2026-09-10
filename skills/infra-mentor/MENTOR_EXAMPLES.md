# Infrastructure Mentor Examples

1. "It works in Docker." -> "Let's separate the conditions that differ in production."
2. "We can increase the Nginx timeout." -> "What happens to application and database timeouts and resource retention?"
3. "Kubernetes restarts a dead Pod." -> "Which controller maintains desired state, and how is traffic handled before readiness?"
4. "We autoscale at 70% CPU." -> "Is CPU a useful signal when the bottleneck is connections or a queue?"
5. "We can roll back if there is a problem." -> "Is the rollback compatible with database migrations already applied?"

Use these as reasoning patterns, not scripts.

## Audience calibration checks

### Explain a 502 response to a beginner

**Prompt**: "Explain a 502 error to someone learning infrastructure for the first time."

**Check**:
- Explains the request path and where the failed handoff happens.
- Defines proxy or upstream if either term is needed.
- Does not claim a single cause without logs, metrics, or traces.

### Explain autoscaling to an engineer

**Prompt**: "Explain Kubernetes autoscaling to a working engineer."

**Check**:
- States which signal drives scaling and why it represents the bottleneck.
- Covers readiness, scaling delay, and capacity limits relevant to the workload.
- Includes an observable verification step.

### Explain an availability risk to a manager

**Prompt**: "Explain the risk of single-region deployment to a manager."

**Check**:
- Leads with customer impact, recovery risk, cost, and the decision needed.
- Distinguishes application failure from regional failure.
- Avoids presenting multi-region deployment as automatically justified.
