# Enterprise Network Consolidation with Regulatory Compliance (HIPAA & PCI DSS)

## Project Scope

- Conducted security assessment of merged financial and healthcare environments  
- Identified high-risk vulnerabilities impacting PHI and cardholder data  
- Performed qualitative risk prioritization (Impact × Likelihood)  
- Designed hybrid cloud architecture to remediate findings  
- Implemented zero trust controls aligned with HIPAA and PCI DSS  

---

## Executive Summary

Following a corporate acquisition, a financial services organization and a healthcare services provider required secure integration of their networks while maintaining regulatory compliance.

The assessment identified critical vulnerabilities including legacy systems, weak authentication controls, exposed remote services, and a publicly accessible database. These issues posed direct risk to Protected Health Information (PHI) and payment card data.

A hybrid cloud architecture was implemented to reduce attack surface, enforce MFA, eliminate public exposure, modernize legacy infrastructure, and align with HIPAA Security Rule and PCI DSS requirements.

---

## Key Security Findings

### Company A – Financial Services

- Weak password policy (8-character minimum, no MFA)  
- Exposed remote services (including RDP)  
- End-of-life Windows Server 2012  
- Inconsistent endpoint standardization  

**Primary Risk:** Credential compromise and regulatory non-compliance.

---

### Company B – Healthcare Services

- No MFA enforcement  
- Internet-accessible PostgreSQL database  
- Windows XP / Windows 7 (EOL)  
- Insecure remote services (Rexec, VNC)  

**Primary Risk:** PHI exposure and HIPAA violation.

---

## Risk Prioritization

Risk ratings were determined using a qualitative Impact × Likelihood model.

| Finding                  | Company | Likelihood | Impact   | Risk Rating |
|--------------------------|---------|------------|----------|-------------|
| Public Database Exposure | B       | High       | Critical | Critical    |
| No MFA                   | B       | High       | High     | High        |
| Weak Password Policy     | A       | Very High  | High     | High        |
| Exposed RDP              | A       | High       | High     | High        |

Risk ratings informed remediation prioritization during integration planning.

---

## Architecture & Remediation Strategy

### Hybrid Cloud Migration
- Migrated application servers to cloud-hosted infrastructure  
- Reduced legacy infrastructure exposure  
- Improved scalability and disaster recovery posture  

### Security Controls Implemented

| Control                 | Purpose                        |
|-------------------------|--------------------------------|
| MFA                     | Prevent credential compromise  |
| Firewall Segmentation   | Reduce lateral movement        |
| VPN Enforcement         | Secure remote access           |
| VLAN Segmentation       | Isolate sensitive environments |
| Private Database Access | Eliminate public exposure      |

---

## Design Principles Applied

**Least Privilege**  
Role-based access controls and segmentation limit unnecessary permissions.

**Defense in Depth**  
Layered controls include firewall inspection, encrypted VPN access, MFA enforcement, and cloud security safeguards.

---

## Regulatory Alignment

**HIPAA**
- Encrypted transmission (VPN/TLS)  
- Segmented workloads  
- Centralized logging  
- Role-based access enforcement  

**PCI DSS**
- Network segmentation  
- Strong authentication controls  
- Firewall configuration management  
- Continuous monitoring  

---

## Residual Risk Considerations

**Ransomware**
- Immutable backups  
- MFA enforcement  
- Endpoint detection and response  

**Cloud Misconfiguration**
- Continuous compliance monitoring  
- Least-privilege enforcement  
- Periodic access reviews  

---

## Financial Analysis

| Model        | Year-One Cost| Primary Tradeoff           |
|--------------|--------------|----------------------------|
| On-Premises  | $20k–$25k    | Limited scalability        |
| Hybrid Cloud | $40k–$45k    | Higher operational expense |

---

## Recommendation

The hybrid cloud model is recommended due to improved scalability, reduced infrastructure lifecycle risk, enhanced disaster recovery capability, and stronger regulatory alignment.

Despite increased operational expenses, long-term risk reduction and compliance posture improvements justify the transition.

---

## Author

Isabel Romero  
M.S. Cybersecurity  
CompTIA PenTest+ | CySA+ | CASP+ (In Progress)

---

## Lessons Learned

- Legacy system management is a primary driver of regulatory exposure.
- Identity controls (MFA enforcement) reduce the majority of initial access risk.
- Segmentation is critical when consolidating regulated environments.
