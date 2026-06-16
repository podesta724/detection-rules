# detection-rules
Splunk and Sigma detections mapped to MITRE ATT&CK, tested against BOTS datasets

Splunk SPL and Sigma detection rules mapped to MITRE ATT&CK, built and tested against the Splunk Boss of the SOC (BOTS) attack datasets. Every rule ships with its logic explained in plain English, true-positive evidence from real attack data, false-positive tuning notes, and response guidance for the analyst who'd catch the alert.

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
| Brute Force - Password Guessing | Credential Access | T1110.001 | — | [rule.yml](rules/credential-access/brute-force-password-guessing/rule.yml) | [rule.spl](rules/credential-access/brute-force-password-guessing/rule.spl) |
| Brute Force - Web CMS Admin Login | Credential Access | T1110.001 | BOTSv1 | [rule.yml](rules/credential-access/brute-force-web-cms-admin/rule.yml) | [rule.spl](rules/credential-access/brute-force-web-cms-admin/rule.spl) |
| Network Service Scanning - Web Vulnerability Scanner | Discovery | T1046 | BOTSv1 | [rule.yml](rules/discovery/network-service-scanning-suricata/rule.yml) | [rule.spl](rules/discovery/network-service-scanning-suricata/rule.spl) |
| Web Shell Access - PHP File Outside CMS Core Paths | Persistence | T1505.003 | BOTSv1 | [rule.yml](rules/persistence/web-shell-iis/rule.yml) | [rule.spl](rules/persistence/web-shell-iis/rule.spl) |
| Web Shell Command Execution via PHP-CGI | Execution | T1059.003 | BOTSv1 | [rule.yml](rules/execution/web-shell-cmd-execution-php-cgi/rule.yml) | [rule.spl](rules/execution/web-shell-cmd-execution-php-cgi/rule.spl) |

*Status: In progress*
