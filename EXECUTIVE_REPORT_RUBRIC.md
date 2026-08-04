# Operation Chimera Cascade: Executive Report Rubric

## Scenario-specific required conclusions

Correlate the hybrid-cloud evidence into phases: initial access, credential use, cloud/source-control actions, and impact. Separate linked events from benign use of valid credentials. Purple-team and maintenance-window artifacts are false signals unless timestamp/device/account evidence connects them. A suspicious login alone is not compromise; require a subsequent action or endpoint corroboration.

## Scoring

- 30% accurate, normalized timeline with artifact citations
- 25% complete entry, pivot, persistence, privilege, and impact analysis
- 20% correct clustering of related, unrelated, benign, and false-signal activity
- 15% disciplined confidence labels and treatment of telemetry gaps
- 10% executive-quality remediation, ownership, and sequencing

## Automatic deductions

- Unsupported attribution or invented observables
- Collapsing every suspicious event into a single incident
- Treating attempted access as successful access
- Treating access as exfiltration without transfer or receipt evidence
- Treating missing logs as proof that activity did not occur
- Omitting material contradictory or benign evidence

Every high-impact conclusion should cite two independent artifacts where available and preserve exact identities, hosts, IP addresses, object names, and timestamps.
