# DT Simulation Evidence Pack

**Factory:** Coo-Cah Garage & Power Electronics Factory, Sagamu, Ogun State  
**Repository:** `coo-cah-factory-electronics-power`  
**Document Ref:** CCG-PE-DT-SIM-001 | **Version:** 1.0  
**Pack Status:** Sprint baseline published; run evidence pending

---

## 1. Purpose

This document locks the first three factory-specific DT simulation scenarios required for readiness
closure. It follows the group experiment-design and KPI-dictionary templates without introducing
factory-local standards.

**Important:** this pack does not claim completed simulation proof. It defines the approved
scenario structure, KPI formulas, baseline windows, and reproducibility placeholders required to
produce auditable evidence.

---

## 2. Scenario Portfolio

| Scenario ID | Scenario | KPI Focus | Current State |
|---|---|---|---|
| SIM-01 | Energy dispatch optimisation — BESS + solar self-sufficiency | kWh / unit, self-sufficiency % | Locked for execution |
| SIM-02 | SMT line OEE / throughput bottleneck simulation | OEE, FPY | Locked for execution |
| SIM-03 | Load bank test queue balancing | Test cycle time, queue depth at 100% load | Locked for execution |

---

## 3. Experiment Design Summary

| Scenario ID | Design Type | Unit of Analysis | Baseline Window | Intervention Window | Confounder Controls |
|---|---|---|---|---|---|
| SIM-01 | Pre/post + matched-control | Day | First 14 days after stable EMS + DT ingestion | First 14 days after approved dispatch model activation | Weather, product mix, generator events, grid availability |
| SIM-02 | Pre/post + matched-control | Shift / line | First 10 stable SMT production days | First 10 intervention shifts after DT bottleneck rules activate | Product mix, staffing, planned downtime, maintenance events |
| SIM-03 | Pre/post + matched-control | Test shift / queue interval | First 10 stable load-bank test days | First 10 intervention days after queue-balancing rules activate | SKU mix, staffing, retest rate, test-bench availability |

---

## 4. KPI Dictionary

| Scenario ID | KPI | Formula | Data Sources | Minimum Proof Threshold |
|---|---|---|---|---|
| SIM-01 | Energy intensity | `total_kwh / good_units_shipped` | EMS sub-meter streams, MES shipment-complete units | Reduction vs. matched-control with approved significance rule |
| SIM-01 | Self-sufficiency % | `((solar_kwh + bess_discharge_kwh) / total_factory_kwh) × 100` | EMS, BESS telemetry, main incomer meter | Improvement vs. matched-control with approved significance rule |
| SIM-02 | OEE | `availability × performance × quality` | MES production events, SMT machine state, quality results | Uplift vs. matched-control with approved significance rule |
| SIM-02 | FPY | `good_units_first_pass / total_units_started` | MES serial records, AOI / ICT / test verdicts | Improvement vs. matched-control with approved significance rule |
| SIM-03 | Test cycle time | `test_end_timestamp - test_start_timestamp` | Load bank test records, MES serial-linked timestamps | Reduction vs. matched-control with approved significance rule |
| SIM-03 | Queue depth at 100% load | `units_waiting_for_test at rated queue checkpoints` | MES queue events, test-bench state | Reduction vs. matched-control with approved significance rule |

---

## 5. Data Quality Gates

| Scenario ID | Completeness Gate | Freshness Gate | Schema Gate |
|---|---|---|---|
| SIM-01 | ≥ 99% on critical energy streams | ≤ 2× nominal update rate | Meter ID, unit, and topic metadata unchanged |
| SIM-02 | ≥ 99% on SMT state and quality streams | ≤ 2× nominal update rate for critical streams | Asset IDs and serial joins validated |
| SIM-03 | ≥ 99% on load-bank and queue events | No missing critical test timestamps | Serial, station, and verdict fields populated |

---

## 6. Reproducibility Package Stub

| Scenario ID | Query / Extract Reference | Intervention Log | Output Artifact | Reviewer Sign-Off |
|---|---|---|---|---|
| SIM-01 | Pending approved EMS + MES extract reference | Pending | Pending | Pending |
| SIM-02 | Pending approved MES + SMT extract reference | Pending | Pending | Pending |
| SIM-03 | Pending approved MES + load-bank extract reference | Pending | Pending | Pending |

---

## 7. Release Rule

No scenario in this pack may be used as DT-ready evidence until:

1. baseline and intervention windows are populated with actual dates,
2. data quality gates are passed,
3. output artifacts are reproducible from source references,
4. reviewer sign-off is recorded.
