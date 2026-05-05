---
name: Supplier Qualification
about: Onboard a new semiconductor, component, or service supplier
title: "[SUPPLIER] "
labels: supplier, procurement
assignees: ""
---

## Supplier Details

| Field | Value |
|---|---|
| **Company Name** | |
| **Country** | |
| **Category** | Semiconductor / Passive Component / PCB / Enclosure / Service / Other |
| **Component(s) Supplied** | |
| **Intended Replacement / Addition** | Replacement for existing supplier / New addition |
| **Existing Supplier (if replacing)** | |

---

## Components / Parts Being Qualified

| Part Number | Description | Annual Volume Estimate | Unit Price (USD/₦) |
|---|---|---|---|
| | | | |
| | | | |

---

## Qualification Checklist

### Documentation

- [ ] Supplier ISO 9001 certificate (or equivalent QMS evidence)
- [ ] Product data sheets and application notes
- [ ] Certificate of Conformance (CoC) format specimen
- [ ] Reliability data (MTBF, AEC-Q100/Q101 qualification, if applicable)
- [ ] REACH / RoHS compliance declaration
- [ ] Country of origin declaration
- [ ] Counterfeit prevention policy (for semiconductors)

### Technical Evaluation

- [ ] Engineering sample received and tested on bench
- [ ] Performance vs. specification verified (datasheet parameters confirmed)
- [ ] Fit-form-function compatibility with existing PCB layout
- [ ] Thermal performance under load bank test conditions
- [ ] Compatibility with current firmware / software drivers

### Supply Chain Assessment

- [ ] Lead time confirmed (standard + allocation-risk scenario)
- [ ] MOQ (Minimum Order Quantity) acceptable
- [ ] Safety stock requirement assessed (see [supply-chain.md](../../docs/supply-chain.md))
- [ ] Shipping mode and logistics route confirmed
- [ ] Form M / SON CoC import requirements reviewed
- [ ] Currency and payment terms agreed
- [ ] Dual-source risk: is this a sole-source? If yes, risk documented.

### Quality & Incoming Inspection

- [ ] Incoming inspection protocol defined (sampling plan, test method)
- [ ] Counterfeit detection procedure (for ICs/semiconductors: CoC + curve tracer/LCR check)
- [ ] MES supplier code created
- [ ] First article inspection (FAI) completed

### Regulatory Compliance

- [ ] Component appears on Coo-Cah approved components list (ACL)
- [ ] NESREA/environmental compliance reviewed (e.g., battery DG classification if applicable)

---

## Risk Assessment

| Risk | Rating (H/M/L) | Mitigation |
|---|---|---|
| Counterfeit risk | | |
| Sole-source dependency | | |
| Lead time volatility | | |
| Geopolitical / logistics | | |
| Quality consistency | | |

---

## Safety Stock Recommendation

| Component | Recommended Safety Stock | Basis |
|---|---|---|
| | | |

---

## Approval

| Role | Name | Date | Decision |
|---|---|---|---|
| Procurement Manager | | | Approve / Reject |
| Quality Manager | | | Approve / Reject |
| Engineering Lead | | | Approve / Reject |

---

## Notes

<!-- Any additional context, test results, or supporting information. -->

---

## Master Repo Reference

> Supplier qualification policy follows the group supply chain doctrine at
> `docs/supply-chain/doctrine.md` in [Coo-Kah-Doks](https://github.com/oumar-code/Coo-Kah-Doks).

- [ ] Approved supplier added to Coo-Cah Approved Vendor List (AVL)
- [ ] Supply chain.md updated if this changes the sourcing strategy
