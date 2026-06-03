# DT Connectivity Proof

**Factory:** Coo-Cah Garage & Power Electronics Factory, Sagamu, Ogun State  
**Repository:** `coo-cah-factory-electronics-power`  
**Document Ref:** CCG-PE-DT-CONN-001 | **Version:** 1.0  
**Artifact Status:** Connectivity proof scaffold published; first live capture pending

---

## 1. Purpose

This document is the factory-local evidence artifact for proving live data connectivity on
critical DT streams. It is required by the DT hard release rule, but publication of this file alone
does **not** satisfy that rule until real capture evidence is attached.

---

## 2. Critical Stream Coverage

| Source Domain | Critical Streams in Scope | Required Proof |
|---|---|---|
| SMT connectors | SMT01-PRINT-SPEED, SMT05-TEMP-Z01, SMT06-DEFECT-RATE | Timestamped value capture + freshness check |
| MES REST events | Serial-linked production and test events | Event receipt timestamp + completeness check |
| EMS / energy streams | ENE01-PV-POWER, ENE03-BESS-SOC, ENE07-MDB-KW | Timestamped value capture + freshness check |

---

## 3. Connectivity Capture Log

| Sensor / Event ID | Source Interface | Last Capture Timestamp | Example Value / Event Ref | Freshness Indicator | Evidence Status |
|---|---|---|---|---|---|
| SMT01-PRINT-SPEED | OPC-UA | Pending live capture | Pending | Pending | Awaiting first capture |
| SMT05-TEMP-Z01 | OPC-UA | Pending live capture | Pending | Pending | Awaiting first capture |
| SMT06-DEFECT-RATE | OPC-UA | Pending live capture | Pending | Pending | Awaiting first capture |
| MES-SERIAL-EVENT | REST API | Pending live capture | Pending | Pending | Awaiting first capture |
| ENE01-PV-POWER | SunSpec / EMS | Pending live capture | Pending | Pending | Awaiting first capture |
| ENE03-BESS-SOC | Modbus TCP / EMS | Pending live capture | Pending | Pending | Awaiting first capture |
| ENE07-MDB-KW | PME API | Pending live capture | Pending | Pending | Awaiting first capture |

---

## 4. Verification Rule

The first live proof package is acceptable only when:

1. each critical stream has a timestamped capture,
2. freshness is within the threshold defined in `sensor-map.md`,
3. the capture source is traceable to the approved connector path,
4. MES / DT owners acknowledge the evidence review.

---

## 5. Hard-Rule Reminder

This factory must **not** be marked DT-ready until:

- mandatory artifacts are complete,
- live connectivity is proven from this artifact with actual evidence,
- three simulations have reproducible evidence lineage.
