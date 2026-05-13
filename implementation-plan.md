# Implementation Plan

**Factory:** Coo-Cah Garage & Power Electronics Factory, Sagamu, Ogun State  
**Repository:** `coo-cah-factory-electronics-power`  
**Document Ref:** CCG-PE-IMPL-001 | **Version:** 1.0

---

## 1. Purpose

This implementation plan defines how the Sagamu Garage & Power Electronics factory moves from
planning to stable Phase 1 execution for inverters, solar charge controllers, UPS, battery
chargers, smart power strips, and power tools.

It aligns with factory baseline documents and the Coo-Kah-Doks group standards for:
- MES-first operations
- Digital twin and AI platform rollout
- Tier 1 critical-infrastructure reliability
- SON/NCC/NESREA/NIPC regulatory readiness

---

## 2. Phase 1 Objectives (2025–2027)

| Objective | Target |
|---|---|
| Civil + utility readiness | Facility, electrical infrastructure, and test zones commissioned |
| Production readiness | SMT, winding, assembly, and load bank lines operational |
| Quality readiness | 100% serial traceability and mandatory pass/fail test gating in MES |
| Compliance readiness | SON/NIS submissions on priority SKUs; NCC path for Wi-Fi models |
| Intra-group readiness | Internal deliveries to sister factories before external scale-up |
| Energy resilience | 600 kWp PV + 700 kWh BESS integrated for ≥80% self-sufficiency |

---

## 3. Workstreams

### 3.1 Industrialisation and Manufacturing

- Commission SMT line and transformer winding/test cells.
- Qualify golden process windows for CCG-INV-PSW 2kVA/3kVA and CCG-SCC-MPPT 40A/60A.
- Stabilise first-pass yield on pilot lots before volume ramp.
- Enforce red-tag NCR loop with re-test control before shipment release.

### 3.2 MES, Digital Twin, and Data Foundation

- Deploy MES as day-1 production system with serial-number lifecycle control.
- Integrate test benches, load banks, Hi-Pot stations, and firmware flashing records.
- Stream operational and energy telemetry to the factory digital twin.
- Establish KPI dashboards: FPY, test pass rate, OEE, energy per unit, and rework rate.

### 3.3 Regulatory and Certification

- Complete NESREA EIA and environmental permit gates before full construction activity.
- Submit SON type-test samples for priority SKUs (CCG-INV-PSW, CCG-SCC-MPPT, CCG-PS).
- Execute NCC pre-compliance and formal type approval path for Wi-Fi products.
- Prepare QMS evidence package for ISO 9001:2015 certification audit.

### 3.4 Supply Chain and Intra-Group Coordination

- Lock 90-day semiconductor safety stock and dual-source policy.
- Operationalise daily enclosure replenishment from Coo-Cah Plastics & Polymers.
- Track import lead-time variability for cores, capacitors, and batteries.
- Prioritise internal allocation for sister factories before external order release.

### 3.5 AI Platform Activation

- Stand up Phase 1 AI capabilities: quality anomaly triage and test-failure clustering.
- Prepare Phase 2 predictive maintenance models on SMT, winding, and load bank assets.
- Define model governance: approvals, rollback, and human sign-off for high-risk decisions.
- Publish monthly AI platform status and deployment risk register.

---

## 4. Delivery Milestones

| Milestone | Window | Exit Criteria |
|---|---|---|
| M1: Site + utility readiness | Q4 2025–Q1 2026 | Power, compressed air, ESD, and safety systems commissioned |
| M2: Equipment commissioning | Q1–Q2 2026 | SMT/winding/load-bank lines pass SAT and capability checks |
| M3: MES + DT integration | Q2 2026 | End-to-end serial traceability and test record linkage active |
| M4: Pilot lot validation | Q3 2026 | Pilot lots meet quality and reliability targets |
| M5: Compliance submissions | Q4 2026 | SON/NCC packages submitted with complete evidence set |
| M6: Internal supply start | Q1 2027 | First approved shipments to sister factories |
| M7: Commercial launch gate | Q2 2027 | Capacity exceeds internal demand with stable quality trend |

---

## 5. Governance and Operating Cadence

| Cadence | Participants | Core Outputs |
|---|---|---|
| Daily production control | Production, quality, maintenance | Throughput, defects, downtime actions |
| Weekly program review | Factory PMO, engineering, supply chain, MES/DT | Risk log, blocked items, milestone status |
| Monthly compliance + AI review | Compliance lead, AI lead, plant leadership | Certification status, AI readiness, control actions |
| Quarterly steering review | Group operations + factory leadership | Phase gates, budget/risk decisions, escalation closures |

---

## 6. Risks and Mitigations

| Risk | Impact | Mitigation |
|---|---|---|
| Semiconductor allocation shocks | Production stoppage risk | 90-day stock, alternate sources, allocation contracts |
| SON/NCC approval delays | Shipment hold on certified SKUs | Early pre-compliance, parallel evidence prep, lab slot pre-booking |
| MES/test integration drift | Traceability gaps, audit risk | Contract tests, go-live rehearsals, hard release gates |
| Grid volatility during commissioning | Lost commissioning time | PV/BESS/genset fallback and critical-load sequencing |
| Intra-group demand spikes | Internal SLA misses | Protected internal buffer and ATP prioritisation rules |

---

## 7. Acceptance Criteria

This plan is considered successfully executed for Phase 1 when:

1. Priority SKUs pass defined quality and reliability thresholds.
2. MES and digital twin provide complete and auditable unit-level records.
3. Compliance pathways (SON/NCC/NESREA) are active and evidence-complete.
4. Intra-group deliveries are stable and on-time.
5. AI platform capabilities are controlled, measurable, and safely integrated into operations.

