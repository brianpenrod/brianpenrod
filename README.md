# Brian Penrod, DBA

I’m the founder of VetOps Financial and a retired U.S. Army Special Forces command sergeant major. I build AI-assisted systems and test what happens when a model’s recommendation can turn into an action. My work focuses on three questions: What can the model decide? What should the system verify? What does the human need to see before approving?

## Start here: SimForge

[SimForge](https://github.com/brianpenrod/simforge) is a robotics simulation prototype. A model proposes a structured plan, validation checks it against the scene, a human reviews it, and a separate evaluator scores execution from simulator telemetry.

The most useful result was a failure. Asked to move a red gear that didn’t exist, the model substituted a real part. The plan passed structural checks, a human approved it, and the simulator moved the substitute. The failure showed why I need to test whether a plan fulfills the original request, not just whether it can execute. Later checks on a frozen candidate are reported separately; they don’t erase the original failure or establish physical robot safety.

[Gate criteria and results](https://github.com/brianpenrod/simforge/blob/main/GATE_METRICS.md) · [Build log](https://github.com/brianpenrod/simforge/blob/main/BUILD_LOG.md)

## Other work

- **Founders Release:** A release-assurance prototype for AI-built software. It ties evidence to a specific commit so a person can make the release decision and know exactly what was reviewed.
- **[MarginCommand](https://vetopsfinancial.com/margincommand):** Job pricing for owner-operated businesses. AI helps surface missing inputs, software calculates pricing and margin, and the owner approves the result.
- **[Finance Operator Toolkit](https://github.com/brianpenrod/finance-operator-toolkit):** Earlier work in variance analysis and financial decision support.

## What I want to test next

Can an independent check catch a mismatch between a user’s request and the proposed action before approval? I’d compare a reviewer who sees the plan alone with one who sees the original request, the plan, and any flagged differences. I’d measure missed substitutions, unnecessary blocks, and review time.
