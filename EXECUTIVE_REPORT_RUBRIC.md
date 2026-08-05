# Operation Chimera Cascade: Executive Report Rubric

## Scenario-specific required conclusions

The primary intrusion combines an AiTM/session-theft and delegated-OAuth track against `e.park` with a developer/supply-chain track against `r.kapoor`. The first track grants a malicious application continuing Graph access and results in access to M&A, board, mail, and diligence data. The second uses a malicious package on the macOS engineering host to steal GitHub access, create a temporary deploy key, push the `hotfix/cache-key` ref, and trigger an innocently approved release workflow.

GitHub OIDC is then used to assume the CI/CD AWS role. The attacker pivots through AWS and EKS, decrypts the production Box export credential, creates or uses an exporter workload, stages the partner dataset, and uploads it to a sanctioned Box location. The external Box download from the same attacker-controlled IP used in the identity/SaaS track is the strongest evidence that the tracks are coordinated and that the exported archive was received externally.

The research-node XMRig activity is malicious but unrelated. `m.sato` compressing finance board packets is approved business activity. Prior purple-team DNS artifacts are stale decoys. Release-signing secrets were reachable, but the supplied evidence contains no signing operation or changed signed artifact; report exposure, not use. Failed MFA against another user is attempted expansion, not proof that account was compromised.

Required reporting distinctions: confirmed versus inferred actions; access versus exfiltration; temporary deploy-key creation versus persistence duration; cloud control-plane visibility versus missing object-level data; and containment priorities for sessions, OAuth grants, developer credentials, GitHub refs, OIDC trust, AWS roles, EKS service accounts, and Box links.

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
