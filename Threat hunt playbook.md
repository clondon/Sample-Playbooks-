# NIST-Based Threat Hunt Playbook

## Purpose
Provide a structured approach for threat hunting based on NIST guidelines, enabling early detection and response to adversarial activities.

## References
- [NIST Cybersecurity Framework (CSF)](https://www.nist.gov/cyberframework)
- [NIST SP 800-61r2: Computer Security Incident Handling Guide](https://csrc.nist.gov/publications/detail/sp/800-61/rev-2/final)

---

## 1. Preparation (NIST CSF: Identify/Protect)
- **Define Hunt Objectives:** What threats, techniques, or assets are the focus?
- **Validate Baselines:** Ensure asset inventory, network diagrams, and normal behavior profiles are up-to-date.
- **Gather Tools & Data Sources:** SIEM, EDR, network logs, endpoint logs, threat intel feeds.

## 2. Hypothesis Development (NIST CSF: Detect)
- **Formulate Hypothesis:** Based on threat intelligence, recent incidents, or environmental changes.
- Example: "An adversary may be using PowerShell to establish persistence."
- **Map Hypothesis to MITRE ATT&CK Techniques.**

## 3. Data Collection and Analysis (NIST CSF: Detect/Respond)
- **Collect Data:** Query relevant logs and telemetry for indicators related to the hypothesis.
- **Analyze Data:** Look for anomalies, suspicious patterns, or known IOCs.
- **Enrich Findings:** Use threat intelligence to validate or expand on suspicious activities.

## 4. Investigation (NIST CSF: Respond)
- **Correlate Events:** Map findings to the kill chain or ATT&CK framework.
- **Deep Dive:** Pivot on suspicious artifacts (hashes, domains, user accounts).
- **Document Findings:** Record evidence, timelines, and affected assets.

## 5. Containment, Eradication, and Recovery (NIST CSF: Respond/Recover)
- **Contain:** Isolate affected systems or accounts.
- **Eradicate:** Remove threats (malware, backdoors).
- **Recover:** Restore systems and validate no residual threats.

## 6. Lessons Learned & Feedback (NIST CSF: Recover)
- **Review Hunt:** What worked, what didn’t?
- **Update Playbook:** Incorporate lessons learned.
- **Share Knowledge:** Report findings to stakeholders and update detection rules.

---

## Example Hunt Scenario

1. **Objective:** Hunt for lateral movement via SMB.
2. **Hypothesis:** Adversaries are using SMB shares to move laterally.
3. **Data Sources:** Windows event logs, network traffic, file access logs.
4. **Analysis:** Search for abnormal SMB connections, new share mounts, unusual file access.
5. **Investigation:** Validate user identities, correlate access times, check for malware.
6. **Containment:** Disable suspicious accounts, block malicious SMB traffic.
7. **Lessons Learned:** Update SMB monitoring and access control policies.

---

## Templates & Checklists

### Hunt Hypothesis Template
- Threat: [Describe]
- Technique: [Map to MITRE ATT&CK]
- Data Sources: [List]
- Expected Artifacts: [List]

### Investigation Checklist
- [ ] Data collected
- [ ] Suspicious activity identified
- [ ] Artifacts validated
- [ ] Containment actions taken
- [ ] Documentation completed

---

## Automation & Improvement
- Integrate hunt processes into SOAR platforms.
- Regularly update playbook as threats evolve.

---

## Appendix
- Links to NIST guidance
- Sample queries
- MITRE ATT&CK mapping resources
