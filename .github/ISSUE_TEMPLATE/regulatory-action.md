---
name: Regulatory Action
about: Track a SON NIS certification, NCC Type Approval, NESREA obligation, or ISO audit action
title: "[REGULATORY] "
labels: regulatory, compliance
assignees: ""
---

## Regulatory Action Details

| Field | Value |
|---|---|
| **Authority** | SON / NCC / NESREA / NIPC / Nigeria Customs / ISO Certification Body / Other |
| **Action Type** | Initial Certification / Surveillance Audit / Type Approval / Permit / Renewal / Corrective Action |
| **Product / Scope** | (e.g., "CCG-INV-PSW 2kVA — NIS 411 certification" or "Factory EIA") |
| **Standard / Regulation** | (e.g., NIS 411, IEC 62040-1, IEC 61683, NESREA EIA Act, ISO 9001:2015) |
| **Certificate / Reference Number** | (if already issued) |
| **Submission Deadline** | |
| **Certificate / Decision Expected** | |
| **Responsible Person** | |

---

## Background

<!-- Describe the context for this regulatory action in 2-5 sentences.
     Reference the relevant section of docs/regulatory.md where applicable. -->

---

## Action Checklist

### Preparation

- [ ] Pre-compliance testing completed (internal load bank / RF lab)
- [ ] Test samples selected and prepared (3–5 units for type tests)
- [ ] Technical documentation package prepared (BOM, schematic, circuit description, user manual)
- [ ] SON CoC for all imported components confirmed (for SON product certification)
- [ ] ISO 9001 evidence package prepared (for SON factory audit)
- [ ] Application fee paid (SON / NCC / NESREA)

### Submission

- [ ] Application submitted to authority
- [ ] Submission reference number obtained: ____________________
- [ ] Confirmation of receipt received from authority

### Authority Review

- [ ] Technical questions / queries from authority responded to
- [ ] Factory audit scheduled (if applicable): date ____________________
- [ ] Factory audit passed / outstanding findings noted (see below)

### Outcome

- [ ] Certificate / approval issued
- [ ] Certificate number recorded in MES (product master + label template)
- [ ] SON C-Mark label template updated (if product certification)
- [ ] NCC label template updated (if NCC Type Approval)
- [ ] docs/regulatory.md updated with certificate number and issue date
- [ ] Annual surveillance / renewal date entered in compliance calendar

---

## Outstanding Findings (from Audit or Assessment)

| Finding | Severity | Due Date | Status |
|---|---|---|---|
| | | | |

---

## Documents Required

| Document | Status | Owner |
|---|---|---|
| Product technical file | ☐ Not started / 🔄 In progress / ✅ Complete | |
| Test report (internal) | ☐ / 🔄 / ✅ | |
| Test report (accredited lab) | ☐ / 🔄 / ✅ | |
| User manual (English) | ☐ / 🔄 / ✅ | |
| Circuit diagram | ☐ / 🔄 / ✅ | |
| Bill of Materials | ☐ / 🔄 / ✅ | |
| Safety data sheets (chemicals) | ☐ / 🔄 / ✅ | |

---

## Certification Impact

| Impact Area | Change Required |
|---|---|
| MES label template | |
| Product label (physical) | |
| Packaging | |
| User manual | |
| Advertising / marketing materials | |
| Export / customs documentation | |

---

## Notes

<!-- Any additional context, authority contacts, consultant details, or risk notes. -->

---

## Master Repo Reference

> This regulatory action is consistent with the group Nigerian regulatory compliance framework.
> See [docs/regulatory.md](../../docs/regulatory.md) for full certification strategy.
> Significant regulatory milestones must be reflected in
> `orchestration/factory-status-registry.md` in [Coo-Kah-Doks](https://github.com/oumar-code/Coo-Kah-Doks).

- [ ] Master repo `factory-status-registry.md` updated with certification status
