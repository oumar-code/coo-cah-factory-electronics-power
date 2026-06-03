# Full Readiness Register

**Factory:** Coo-Cah Garage & Power Electronics Factory, Sagamu, Ogun State  
**Repository:** `coo-cah-factory-electronics-power`  
**Document Ref:** CCG-PE-READY-001 | **Version:** 1.0  
**Authoritative Status Date:** 2026-05-13

---

## 1. Purpose and Source of Truth

This register is the **authoritative readiness tracker** for the remaining operational passes required
for full factory launch readiness.

It resolves the baseline inconsistency between:

- `docs/gap-closure-report.md`, which closes the **supplementary documentation** cycle, and
- the still-open **operational readiness passes** for BIM, sensors, pentest execution, and AI
  production go-live.

**Authoritative rule:** where operational readiness status is concerned, this register overrides
summary wording in older documents.

---

## 2. Week 0 Baseline Reconciliation

| Item | Decision |
|---|---|
| Canonical tracker | This document is the single readiness register for Pass 7A, 7B, 8, 9, and 10 |
| Documentation-cycle closure | `docs/gap-closure-report.md` remains valid for supplementary-document closure only |
| BIM evidence set | `docs/bim/zone-boundaries.md` and `docs/bim/asset-anchors.md` hold the current design baseline pending IFC sign-off |
| Sensor evidence set | `docs/sensor-map.md` holds the current authoritative registry baseline |
| Security evidence set | `docs/pentest-scoping.md` holds scope, execution plan, findings governance, and closure gates |
| AI evidence set | `docs/ai-platform-status.md` holds production go-live readiness, cutover, rollback, and hypercare controls |

**Week 0 gate status:** ✅ Closed — baseline reconciled and evidence locations defined.

---

## 3. Readiness Register

| Pass | Workstream | Status | Owner | Target Date | Dependencies | Evidence Artifact |
|---|---|---|---|---|---|---|
| Gate 0 | Baseline reconciliation and governance setup | ✅ Closed | Program Manager | 2026-05-13 | None | This register + updated gap report |
| Pass 7A | BIM zone boundary population | 🟡 In progress | Digital Twin Lead | 2026-06-06 | Approved site CRS, floor-zone naming, IFC package issue | [BIM Zone Boundaries](./bim/zone-boundaries.md) |
| Pass 7B | BIM asset anchor population | 🟡 In progress | Controls Engineering Lead | 2026-06-13 | Pass 7A baseline, equipment tag freeze, install walkdown pack | [BIM Asset Anchors](./bim/asset-anchors.md) |
| Pass 8 | Full sensor registry population | 🟡 In progress | MES / OT Integration Lead | 2026-06-27 | Pass 7A + 7B baseline, OT inventory export, MQTT/OPC-UA mapping | [Sensor Registry](./sensor-map.md) |
| Pass 9 | Pentest execution and findings closure | 🟠 Planned | Security Manager | 2026-07-18 | Pass 8 asset inventory, approved ROE, test-window approval, temporary credentials | [Pentest Scoping](./pentest-scoping.md) |
| Pass 10 | AI platform production go-live | 🟠 Planned | AI Platform Lead | 2026-08-07 | Pass 9 blocking findings dispositioned, prod IAM ready, SLO dashboards live | [AI Platform Status](./ai-platform-status.md) |

---

## 4. Sequencing and Phase Gates

| Sequence | Gate Rule | Release Condition |
|---|---|---|
| 7A → 7B | No asset anchors published against unstable zone geometry | Zone IDs, polygons, and CRS frozen in BIM baseline |
| 7B → 8 | No sensor registry promotion without mapped asset anchors | All fixed in-scope assets have anchor IDs and zone assignments |
| 8 → 9 | No pentest execution against incomplete asset inventory | In-scope systems, endpoints, and service accounts enumerated |
| 9 → 10 | No AI production cutover with unresolved blocking security exposure | Critical/high findings closed or formally risk-accepted |

**Weekly governance cadence:** Wednesday readiness board, single RAG review, owner-by-owner blocker review,
and evidence-link verification.

---

## 5. Acceptance Criteria by Pass

### Pass 7A — BIM Zone Boundaries

Pass 7A is accepted only when:

1. All in-scope building and site zones have closed polygons in the approved site-local CRS.
2. Zone IDs match the floor-plan and DT taxonomy with no duplicates.
3. Boundary QA confirms no overlaps, no orphan zones, and 100% coverage of the approved scope.
4. DT and MES stakeholders sign off the import-ready dataset.

### Pass 7B — BIM Asset Anchors

Pass 7B is accepted only when:

1. Every fixed in-scope asset has an anchor ID tied to an existing asset tag.
2. Coordinates include x/y/z and orientation with one authoritative record per asset tag.
3. QA confirms no duplicate anchors, no missing fixed assets, and no orientation nulls.
4. The anchor registry is signed off for production publication.

### Pass 8 — Sensor Registry

Pass 8 is accepted only when:

1. Every production-relevant telemetry point has a single authoritative sensor ID.
2. Asset, zone, protocol, topic/node, unit, owner, and criticality are populated.
3. Registry status distinguishes active, planned, reserved, and decommissioned points.
4. Ingestion readiness and data quality baselines are documented and approved.

### Pass 9 — Pentest Execution

Pass 9 is accepted only when:

1. All in-scope target groups have executed results and severity-rated findings.
2. Every critical/high finding has an owner, remediation action, and target closure date.
3. Retest scope is agreed for all blocking findings.
4. Residual risk is formally signed by security and factory leadership.

### Pass 10 — AI Platform Production Go-Live

Pass 10 is accepted only when:

1. Production endpoints, IAM, and service accounts are active and least-privilege reviewed.
2. SLO dashboards, alerting, and rollback playbooks are exercised successfully.
3. Shadow/parallel verification completes without unresolved blocking variance.
4. Hypercare closes with stable service metrics and documented operational ownership.

---

## 6. Current Blockers

| Blocker | Affects | Current Handling |
|---|---|---|
| Final IFC model issue package not yet attached to repository evidence set | Pass 7A / 7B | Current BIM docs hold design baseline and import schema pending final issue |
| OT export and MQTT/OPC-UA point list not yet signed by controls and MES teams | Pass 8 | Sensor registry is populated as authoritative design baseline pending final walkdown |
| Pentest windows and temporary credential pack not yet approved | Pass 9 | Scope is fixed; execution tracker and findings governance are preloaded |
| Production IAM/service-account promotion for AI endpoints not yet signed | Pass 10 | Go-live checklist and rollback plan are defined but not yet released |

---

## 7. Definition of Done for Full Readiness

Full readiness is achieved only when:

1. Zone, anchor, and sensor coverage reach 100% of the approved scope.
2. Pentest critical/high findings are either closed or formally risk-accepted.
3. AI production endpoints are live with monitored SLOs and tested rollback.
4. This register and linked evidence artifacts show **✅ Closed** for Pass 7A, 7B, 8, 9, and 10.

---

## 8. DT Go / No-Go Checklist

- [ ] Pass 7A evidence package includes IFC import proof, geometry QA, and DT/MES sign-off
- [ ] Pass 7B evidence package includes walkdown confirmation and production publication approval
- [ ] Pass 8 OT export, connector ownership, and ingestion freshness/completeness checks are signed
- [ ] Pass 9 critical/high findings are closed or formally risk-accepted
- [ ] Pass 10 production IAM, SLO dashboards, rollback test, and hypercare ownership are complete
- [ ] Three DT simulations have locked KPI definitions and reproducible evidence lineage
- [ ] Live connectivity proof is published for critical streams before any DT-ready declaration

**Decision rule:** if any checklist item remains open, DT-ready status remains blocked.

---

## 9. Two-Week Sprint Deliverables (2026-06-03 → 2026-06-17)

| Deliverable | Owner | Target Date | Status |
|---|---|---|---|
| BIM evidence pack overview published | Digital Twin Lead | 2026-06-04 | ✅ Complete |
| DT pilot evidence-pack scaffolding published | DT Engineering Lead | 2026-06-05 | ✅ Complete |
| Weekly DT/MES/OT review log activated | PMO | 2026-06-05 | ✅ Complete |
| Pass 7A sign-off package attached and reviewed | Digital Twin Lead | 2026-06-06 | 🟡 In progress |
| Pass 7B walkdown package prepared | Controls Engineering Lead | 2026-06-13 | 🟡 In progress |
| Pass 8 OT export and connector sign-off pack updated | MES / OT Integration Lead | 2026-06-17 | 🟡 In progress |
| Three-scenario simulation evidence pack published | DT Engineering Lead | 2026-06-17 | ✅ Complete |
| First connectivity proof artifact published | MES Product Owner | 2026-06-17 | ✅ Complete |

---

## 10. Escalation Rule

Any blocker that threatens Pass 7A close by **2026-06-06** must be escalated to the Group CTO
within **1 business day**. Because Passes 7A → 7B → 8 → 9 → 10 are hard-sequenced, a slip in Pass
7A puts the entire DT readiness chain at risk.

---

## 11. Related Documents

- [Gap Closure Report](./gap-closure-report.md)
- [BIM Zone Boundaries](./bim/zone-boundaries.md)
- [BIM Asset Anchors](./bim/asset-anchors.md)
- [Sensor Registry](./sensor-map.md)
- [Pentest Scoping](./pentest-scoping.md)
- [AI Platform Status](./ai-platform-status.md)
- [DT Weekly Review Log](./dt-weekly-review-log.md)
- [DT Simulation Evidence Pack](./dt-simulation-evidence-pack.md)
- [DT Connectivity Proof](./dt-connectivity-proof.md)
