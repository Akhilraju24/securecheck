# Control mapping

The requirement behind each assessment question. This is the reference a reviewer
should read to understand what SecureCheck actually tests.

<!-- TODO: fill the ISO and BSI clause columns from your dissertation.
     The NIS2 column is already precise because the questions cite sub-articles. -->

## ISO/IEC 27001

| ID | Question area | Clause / Annex A control |
|---|---|---|
| i1 | Information Security Policy | Clause 5.2 |
| i2 | ISMS scope definition | Clause 4.3 |
| i3 | Annual risk assessment | Clause 6.1.2 |
| i4 | Risk treatment plan | Clause 6.1.3 |
| i5 | Roles and responsibilities | Clause 5.3 |
| i6 | Security awareness training | |
| i7 | Asset inventory | |
| i8 | Access control | |
| i9 | Malware protection | |
| i10 | Backup and restoration testing | |
| i11 | Incident management procedure | |
| i12 | Supplier security assessment | |
| i13 | Encryption at rest and in transit | |
| i14 | Physical access controls | |
| i15 | Internal audit | Clause 9.2 |

## NIS2 — Article 21 risk management measures

| ID | Question area | Article |
|---|---|---|
| n1 | Cybersecurity risk management policies | 21(a) |
| n2 | Business continuity and disaster recovery | 21(b) |
| n3 | Incident detection and reporting timelines | 21(c) |
| n4 | Supply chain security | 21(d) |
| n5 | Security in acquisition, development, maintenance | 21(e) |
| n6 | Effectiveness measurement | 21(f) |
| n7 | Cyber hygiene and awareness training | 21(g) |
| n8 | Cryptography | 21(h) |
| n9 | Personnel security and privileged access | 21(i) |
| n10 | Multi-factor authentication | 21(j) |

## BSI IT-Grundschutz

| ID | Question area | Standard |
|---|---|---|
| b1 | Baseline analysis | BSI-Standard 200-2 |
| b2 | Compendium module adoption | IT-Grundschutz-Kompendium |
| b3 | Protection requirement classification | BSI-Standard 200-2 |
| b4 | IT-Sicherheitsbeauftragter | BSI-Standard 200-1 |
| b5 | Sicherheitskonzept | BSI-Standard 200-2 |

## Cross-framework overlaps

Several requirements recur across frameworks and are currently assessed by
separate questions:

| Requirement | ISO | NIS2 |
|---|---|---|
| Awareness training | i6 | n7 |
| Supply chain security | i12 | n4 |
| Cryptography | i13 | n8 |
| Incident management | i11 | n3 |
| Risk management | i3, i4 | n1 |

<!-- TODO: see the "possible next step" note in the README discussion —
     merging these into single questions tagged to multiple frameworks would
     shorten the assessment and let one answer satisfy several controls. -->
