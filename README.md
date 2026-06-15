# detection-rules
Splunk and Sigma detections mapped to MITRE ATT&CK, tested against BOTS datasets

Splunk SPL and Sigma detection rules mapped to MITRE ATT&CK, built and tested against the Splunk Boss of the SOC (BOTS) attack datasets. Every rule ships with its logic explained in plain English, true-positive evidence from real attack data, false-positive tuning notes, and response guidance for the analyst who'd catch the alert. The goal isn't a pile of queries — it's detections documented the way a real SOC would need them.

## Structure

```
rules/
└── <tactic>/
    └── <rule-name>/
        ├── rule.spl   # Splunk SPL search
        └── rule.yml   # Sigma rule with ATT&CK mapping, evidence, and response guidance
```

## Detection Index

| Rule | Tactic | Technique | Dataset | Sigma | SPL |
|------|--------|-----------|---------|-------|-----|
| Brute Force - Password Guessing | Credential Access | T1110.001 | BOTSv1 | [rule.yml](rules/credential-access/brute-force-password-guessing/rule.yml) | [rule.spl](rules/credential-access/brute-force-password-guessing/rule.spl) |

*Status: In progress — first batch of rules landing soon.*
