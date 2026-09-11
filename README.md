Markdown
# SOC SSH Log Investigation
A self-directed SOC Tier 1 training project analyzing simulated SSH authentication logs to identify brute-force login attempts, using two independent methods: Linux command-line tools and Splunk Enterprise (SIEM).
## What this project covers
**Log triage** using 'grep', 'awk', 'sort', and 'uniq' to indentify failed login patterns
**SIEM analysis** using Splunk enterprise, including data ingestion and SPL queries ('rex' field extraction, stats aggregation)
**incident documentation** - a formal SOC incident report covering observation, evidence, analysis, and recommended action
## Key Finding
Two source IPs showed brute-force login patterns against the 'root' and admin account
| Source IP | Failed Attempts |
|---|---|
| 185.220.101.4 | 3 |
| 45.155.205.77 | 2 |
This result was confirmed identically using both the command-line and pipeline and Splunk SPL, validating the finding across tools
## Tools Used
Kali Linux, grep, awk, Splunk Enterprise, SPL
## Failed in this repo
- 'auth.log' - sample SSH authentication log analyzed
- 'commands.md' - command-line and SPL queries used
- 'SOC_incident_report.pdf' - formal incident write-up
- Splunk_SIEM_Lab_Report.pdf' Splunk setup and analysis write-up
