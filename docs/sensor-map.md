# Sensor Registry

**Factory:** Coo-Cah Garage & Power Electronics Factory, Sagamu, Ogun State  
**Repository:** `coo-cah-factory-electronics-power`  
**Document Ref:** CCG-PE-SENS-001 | **Version:** 1.0  
**Registry Status:** Design baseline populated; pending OT export and controls sign-off

---

## 1. Registry Standard

This document is the authoritative sensor registry baseline for DT/MES ingestion readiness.

**Required fields per sensor point**
- authoritative sensor ID
- asset tag or zone
- protocol and topic / node
- engineering unit
- nominal update rate
- owner
- criticality
- lifecycle status

**Lifecycle status values**
- `Active` — expected at launch
- `Planned` — defined but not yet commissioned
- `Reserved` — ID held for near-term expansion
- `Decommissioned` — retired; never reuse ID

---

## 2. Sensor Register

| Sensor ID | Asset / Zone | Description | Protocol / Topic or Node | Unit | Update Rate | Owner | Criticality | Status | Consumer |
|---|---|---|---|---|---|---|---|---|---|
| ENV-A-TEMP-01 | ZONE-A | SMT zone ambient temperature | Modbus TCP / `env/zone-a/temp-01` | °C | 30 s | Facilities | High | Active | MES + DT |
| ENV-A-RH-01 | ZONE-A | SMT zone ambient humidity | Modbus TCP / `env/zone-a/rh-01` | %RH | 30 s | Facilities | High | Active | MES + DT |
| ENV-A-DP-01 | ZONE-A | SMT zone differential pressure | BACnet / `env/zone-a/dp-01` | Pa | 30 s | Facilities | Medium | Active | DT |
| SMT01-PRINT-SPEED | SMT-01 | Printer cycle speed | OPC-UA / `ns=4;s=SMT01.PrintSpeed` | boards/h | 5 s | SMT Engineering | High | Active | MES + DT |
| SMT01-SQUEEGEE-PRESS | SMT-01 | Closed-loop squeegee pressure | OPC-UA / `ns=4;s=SMT01.SqueegeePressure` | N | 5 s | SMT Engineering | High | Active | DT |
| SMT02-PASTE-VOLUME | SMT-02 | SPI paste volume result | OPC-UA / `ns=4;s=SMT02.PasteVolume` | % of target | Per board | SMT Engineering | High | Active | MES + DT |
| SMT02-PASTE-HEIGHT | SMT-02 | SPI paste height result | OPC-UA / `ns=4;s=SMT02.PasteHeight` | µm | Per board | SMT Engineering | High | Active | MES + DT |
| SMT02-BOARD-RESULT | SMT-02 | SPI board pass/fail | OPC-UA / `ns=4;s=SMT02.BoardResult` | pass/fail | Per board | SMT Engineering | High | Active | MES |
| SMT03-CPH | SMT-03 | High-speed placement rate | Yamaha API / `smt03/cph` | cph | 5 s | SMT Engineering | High | Active | DT |
| SMT03-NOZZLE-ERR | SMT-03 | Nozzle pick error count | Yamaha API / `smt03/nozzle_error` | count | 5 s | SMT Engineering | High | Active | DT |
| SMT03-FEEDER-ERR | SMT-03 | Feeder error count | Yamaha API / `smt03/feeder_error` | count | 5 s | SMT Engineering | Medium | Active | DT |
| SMT04-CPH | SMT-04 | Flexible placement rate | Yamaha API / `smt04/cph` | cph | 5 s | SMT Engineering | High | Active | DT |
| SMT04-NOZZLE-ERR | SMT-04 | Nozzle pick error count | Yamaha API / `smt04/nozzle_error` | count | 5 s | SMT Engineering | Medium | Active | DT |
| SMT04-FEEDER-ERR | SMT-04 | Feeder error count | Yamaha API / `smt04/feeder_error` | count | 5 s | SMT Engineering | Medium | Active | DT |
| SMT05-TEMP-Z01 | SMT-05 | Reflow zone temperature array (`Z01..Z10`) | OPC-UA / `ns=4;s=SMT05.ZoneTemp[1..10]` | °C | 2 s | SMT Engineering | High | Active | MES + DT |
| SMT05-CONV-SPEED | SMT-05 | Reflow conveyor speed | OPC-UA / `ns=4;s=SMT05.ConveyorSpeed` | mm/min | 2 s | SMT Engineering | High | Active | DT |
| SMT05-O2 | SMT-05 | Reflow atmosphere oxygen | OPC-UA / `ns=4;s=SMT05.OxygenPct` | % | 2 s | SMT Engineering | Medium | Active | DT |
| SMT06-DEFECT-RATE | SMT-06 | AOI defect count by board | OPC-UA / `ns=4;s=SMT06.DefectRate` | defects/board | Per board | Quality Engineering | High | Active | MES + DT |
| SMT07-SOLDER-TEMP | SMT-07 | Wave solder bath temperature | OPC-UA / `ns=4;s=SMT07.SolderTemp` | °C | 5 s | SMT Engineering | High | Active | DT |
| SMT07-WAVE-HEIGHT | SMT-07 | Wave height | OPC-UA / `ns=4;s=SMT07.WaveHeight` | mm | 5 s | SMT Engineering | Medium | Active | DT |
| SMT07-FLUX-FLOW | SMT-07 | Flux volume flow | OPC-UA / `ns=4;s=SMT07.FluxFlow` | ml/min | 5 s | SMT Engineering | Medium | Active | DT |
| SMT08-ICT-RESULT | SMT-08 | ICT verdict | TCP API / `ict/result` | pass/fail | Per board | Quality Engineering | High | Active | MES |
| SMT08-TEST-TIME | SMT-08 | ICT test duration | TCP API / `ict/test_time` | s | Per board | Quality Engineering | Medium | Active | MES |
| SMT09-SPINDLE-SPEED | SMT-09 | Router spindle speed | OPC-UA / `ns=4;s=SMT09.SpindleSpeed` | rpm | 5 s | SMT Engineering | Medium | Active | DT |
| SMT09-DUST-PRESS | SMT-09 | Dust extraction pressure | Modbus TCP / `dust/smt09/pressure` | Pa | 10 s | Facilities | Medium | Active | DT |
| WND01-TURNS | WND-01 | Toroidal turns count | OPC-UA / `ns=4;s=WND01.Turns` | count | Per unit | Winding Engineering | High | Active | MES + DT |
| WND01-TENSION | WND-01 | Toroidal wire tension | OPC-UA / `ns=4;s=WND01.Tension` | N | 2 s | Winding Engineering | High | Active | DT |
| WND02-TURNS | WND-02 | EI winding turns count | OPC-UA / `ns=4;s=WND02.Turns` | count | Per unit | Winding Engineering | High | Active | MES + DT |
| WND02-TENSION | WND-02 | EI winding wire tension | OPC-UA / `ns=4;s=WND02.Tension` | N | 2 s | Winding Engineering | High | Active | DT |
| WND05-VACUUM | WND-05 | Varnish tank vacuum level | Modbus TCP / `wnd05/vacuum` | mbar | 5 s | Winding Engineering | High | Active | DT |
| WND05-TEMP | WND-05 | Varnish tank temperature | Modbus TCP / `wnd05/temp` | °C | 5 s | Winding Engineering | Medium | Active | DT |
| WND06-TURNS-RATIO | WND-06 | Transformer turns ratio | Ethernet API / `wnd06/turns_ratio` | ratio | Per unit | Test Engineering | High | Active | MES + DT |
| WND06-DCR | WND-06 | Transformer DC resistance | Ethernet API / `wnd06/dcr` | mΩ | Per unit | Test Engineering | High | Active | MES + DT |
| WND06-HIPOT-RESULT | WND-06 | Transformer Hi-Pot result | Ethernet API / `wnd06/hipot_result` | pass/fail | Per unit | Test Engineering | High | Active | MES |
| WND07-PD-PC | WND-07 | Partial discharge magnitude | Ethernet API / `wnd07/pd_pc` | pC | Per unit | Test Engineering | Medium | Planned | DT |
| TST01-LOAD-KW | TST-01 | Load bank active power | Modbus TCP / `tst01/load_kw` | kW | 1 s | Test Engineering | High | Active | MES + DT |
| TST01-OUTPUT-V | TST-01 | Output voltage | Modbus TCP / `tst01/output_v` | V | 1 s | Test Engineering | High | Active | MES + DT |
| TST01-OUTPUT-I | TST-01 | Output current | Modbus TCP / `tst01/output_i` | A | 1 s | Test Engineering | High | Active | MES + DT |
| TST01-FREQ | TST-01 | Output frequency | Modbus TCP / `tst01/freq` | Hz | 1 s | Test Engineering | High | Active | MES + DT |
| TST01-DURATION | TST-01 | Test duration timer | Modbus TCP / `tst01/duration` | s | 1 s | Test Engineering | Medium | Active | MES |
| TST02-THD | TST-02 | Power quality THD | Modbus TCP / `tst02/thd` | % | 1 s | Test Engineering | High | Active | MES + DT |
| TST02-PF | TST-02 | Power factor | Modbus TCP / `tst02/pf` | ratio | 1 s | Test Engineering | Medium | Active | MES + DT |
| TST05-HIPOT-LEAK | TST-05 | Hi-Pot leakage current | Ethernet API / `tst05/leakage` | mA | Per test | Test Engineering | High | Active | MES |
| TST05-HIPOT-RESULT | TST-05 | Hi-Pot verdict | Ethernet API / `tst05/result` | pass/fail | Per test | Test Engineering | High | Active | MES |
| TST08-MPPT-EFF | TST-08 | MPPT efficiency | Ethernet API / `tst08/mppt_eff` | % | Per test | Test Engineering | High | Active | MES + DT |
| TST08-CHARGE-ERR | TST-08 | Charge-current accuracy error | Ethernet API / `tst08/charge_err` | % | Per test | Test Engineering | High | Active | MES |
| TST09-XFER-TIME | TST-09 | UPS transfer time | Ethernet API / `tst09/transfer_ms` | ms | Per test | Test Engineering | High | Active | MES |
| TST10-PEAK-TEMP | TST-10 | Thermal scan peak temperature | USB API / `tst10/peak_temp` | °C | Per scan | Quality Engineering | High | Active | MES + DT |
| TST12-CHAMBER-TEMP | TST-12 | Environmental chamber profile | Modbus TCP / `tst12/temp_profile` | °C | 10 s | Reliability Engineering | Medium | Planned | DT |
| TST13-LCR | TST-13 | L/C/R/ESR result bundle | SCPI / `tst13/lcr_bundle` | structured | Per test | Test Engineering | Medium | Active | MES |
| ENV-I-TEMP-01 | ZONE-I | Component store temperature | Modbus TCP / `env/zone-i/temp-01` | °C | 30 s | Facilities | High | Active | DT |
| ENV-I-RH-01 | ZONE-I | Component store humidity | Modbus TCP / `env/zone-i/rh-01` | %RH | 30 s | Facilities | High | Active | DT |
| ENV-J-TEMP-01 | ZONE-J | Server room temperature | Modbus TCP / `env/zone-j/temp-01` | °C | 15 s | IT Infrastructure | High | Active | DT + alerting |
| ENV-J-RH-01 | ZONE-J | Server room humidity | Modbus TCP / `env/zone-j/rh-01` | %RH | 15 s | IT Infrastructure | Medium | Active | DT + alerting |
| FAC02-AIR-PRESS | FAC-02 | Compressed air ring-main pressure | Modbus TCP / `utilities/air/pressure` | bar | 10 s | Facilities | Medium | Active | DT |
| FAC02-AIR-DEWPT | FAC-02 | Compressed air dewpoint | Modbus TCP / `utilities/air/dewpoint` | °C | 30 s | Facilities | Medium | Active | DT |
| ENE01-PV-POWER | ENE-01 | Solar array output power | SunSpec / `solar/pv_power` | kW | 60 s | Energy Manager | High | Active | DT + EMS |
| ENE01-STRING-ALARM | ENE-01 | Solar string alarm state | SunSpec / `solar/string_alarm` | state | 60 s | Energy Manager | Medium | Active | DT + EMS |
| ENE03-BESS-SOC | ENE-03 | BESS state of charge | Modbus TCP / `bess/soc` | % | 60 s | Energy Manager | High | Active | DT + EMS |
| ENE03-BESS-PWR | ENE-03 | BESS charge/discharge power | Modbus TCP / `bess/power_kw` | kW | 60 s | Energy Manager | High | Active | DT + EMS |
| ENE03-BESS-TEMP | ENE-03 | BESS container temperature | Modbus TCP / `bess/temp` | °C | 60 s | Energy Manager | High | Active | DT + EMS |
| ENE04-ATS-POS | ENE-04 | ATS source position | Modbus TCP / `power/ats/position` | enum | 5 s | Energy Manager | High | Active | DT + alerting |
| ENE05-GEN-RUNHRS | ENE-05 | Generator runtime hours | Modbus TCP / `gen/run_hours` | h | 60 s | Facilities | Medium | Active | DT + EMS |
| ENE05-FUEL-LVL | ENE-05 | Generator fuel level | Modbus TCP / `gen/fuel_level` | % | 60 s | Facilities | Medium | Active | DT + EMS |
| ENE06-PF | ENE-06 | Main power factor | Modbus TCP / `power/pf` | ratio | 60 s | Energy Manager | Medium | Active | DT + EMS |
| ENE07-MDB-KW | ENE-07 | Main incomer active power | PME API / `meters/mdb/kw` | kW | 60 s | Energy Manager | High | Active | DT + EMS |
| ENE07-SMDB-A-KW | ENE-07 | SMT sub-board active power | PME API / `meters/smdb-a/kw` | kW | 60 s | Energy Manager | Medium | Active | DT + EMS |
| ENE07-SMDB-C-KW | ENE-07 | Assembly and test sub-board power | PME API / `meters/smdb-c/kw` | kW | 60 s | Energy Manager | Medium | Active | DT + EMS |

---

## 3. Ingestion Readiness Matrix

| Source Domain | Protocol | Point Coverage | Target Consumer | Readiness | Blocking Item |
|---|---|---|---|---|---|
| SMT line | OPC-UA + Yamaha API | 23 logical streams | MES + DT | Ready for mapping | Final endpoint whitelist approval |
| Winding cell | OPC-UA + Ethernet API | 10 logical streams | MES + DT | Ready for mapping | Walkdown confirmation for WND-07 deployment |
| Test zone | Modbus TCP + Ethernet API + SCPI | 15 logical streams | MES + DT | Ready for mapping | Final test bench IP allocation |
| Environment / utilities | Modbus TCP + BACnet | 8 logical streams | DT + alerting | Ready for mapping | BMS point export sign-off |
| Energy systems | SunSpec + Modbus TCP + PME API | 12 logical streams | DT + EMS | Ready for mapping | EMS credential release |

---

## 4. Data Quality Baseline

| Quality Dimension | Target | Current Baseline Rule |
|---|---|---|
| Completeness | ≥ 99% for high-criticality points | Alert if any high-criticality point misses 3 consecutive intervals |
| Freshness | ≤ 2× nominal update rate | Mark stale in DT and block AI consumers on stale high-criticality data |
| Unit consistency | 100% | No ingest if unit metadata is absent or changed without approval |
| ID uniqueness | 100% | Reject duplicate sensor IDs in registry promotion |
| Ownership coverage | 100% | Every sensor must have accountable owner before activation |

---

## 5. Acceptance Gate

This registry is ready for operational closure when:

1. controls and MES teams sign the OT export,
2. all active points are connected to validated assets and zones,
3. and the ingestion pipeline passes completeness and freshness checks.

---

## 6. Pass 8 Execution Tracker

| Item | Owner | Target Date | Status | Notes |
|---|---|---|---|---|
| OT inventory export attached to evidence pack | MES / OT Integration Lead | 2026-06-17 | Pending | Required before Pass 8 close |
| MQTT/OPC-UA point-list signed by controls and MES teams | MES / OT Integration Lead | 2026-06-17 | Pending | Required to move from mapping to activation |
| WND07-PD-PC commissioning decision recorded | Test Engineering Lead | 2026-06-17 | Deferred pending WND-07 walkdown | Sensor remains `Planned` until deployment window is approved |
| TST12-CHAMBER-TEMP commissioning decision recorded | Reliability Engineering Lead | 2026-06-17 | Deferred pending chamber commissioning | Sensor remains `Planned` until test chamber is in service |
| Completeness and freshness checks executed on critical streams | MES Product Owner | 2026-06-27 | Pending | Final Pass 8 closure evidence |

**Decision note:** the two `Planned` points are formally deferred in this sprint. They remain in the
authoritative registry and require explicit promotion review before activation.

---

## 7. Related Documents

- [Full Readiness Register](./readiness-register.md)
- [DT Connectivity Proof](./dt-connectivity-proof.md)
- [BIM Asset Anchors](./bim/asset-anchors.md)
- [Digital Twin](./digital-twin.md)
- [MES Integration](./mes-integration.md)
