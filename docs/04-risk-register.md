## 04 – Risk Register

## Risk Management Approach
All risks are identified, assessed, and documented in accordance with the governance framework defined in the Project Charter. Risks are evaluated using qualitative scoring based on probability and impact.

### Risk Rating Scale
- Probability: 1 (Very Low) – 5 (Very High)
- Impact: 1 (Minimal) – 5 (Severe)
- Risk Score = Probability × Impact

## Risk Register
| ID  | Risk Description | Category | Probability | Impact | Score | Mitigation Strategy | Owner | Status |
|-----|------------------|----------|------------|--------|-------|--------------------|-------|--------|
| R-001 | Proxmox host hardware failure | Technical | 3 | 5 | 15 | Weekly VM backups to external SSD; snapshot schedule | IT Admin | Open |
| R-002 | Firewall misconfiguration exposing services | Security | 2 | 5 | 10 | Default deny WAN; no public port forwarding | Security Admin | Mitigated |
| R-003 | VM resource exhaustion | Operational | 3 | 3 | 9 | Resource monitoring; memory and CPU allocation limits | SysAdmin | Monitoring |
| R-004 | Insufficient log retention | Security | 2 | 4 | 8 | Define log retention policy; validate storage capacity | Security Analyst | Open |
| R-005 | Documentation drift from implementation | Project | 2 | 4 | 8 | Weekly documentation review checkpoint | Project Manager | Open |

## Risk Review Process
Risks are reviewed:
- At each major milestone
- After significant infrastructure changes
- Prior to capstone submission
