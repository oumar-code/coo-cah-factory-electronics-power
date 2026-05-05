# Machinery & Equipment Register

**Factory:** Coo-Cah Garage & Power Electronics Factory, Sagamu, Ogun State
**Document Ref:** CCG-PE-MACH-001 | **Version:** 1.0 | **Phase:** 1

> This equipment register covers all production, test, material handling, and energy systems
> for Phase 1. It is consistent with the master repo blueprint at
> `factories/electronics/garage-power-electronics/` in [Coo-Kah-Doks](https://github.com/oumar-code/Coo-Kah-Doks).

---

## 1. SMT (Surface Mount Technology) PCB Production Line

The SMT line produces all inverter control PCBs, MPPT solar charge controller boards, UPS control
boards, and smart power strip PCBs in-house. In-house SMT production is strategic: it eliminates
dependence on external PCB assembly houses, enables rapid design iterations, and allows full
traceability from bare board to finished product.

### 1.1 Line Configuration

```
Bare Board In-feed
      ↓
  SPI (Solder Paste Inspection)
      ↓
  Solder Paste Printer
      ↓
  Pick & Place #1 (high-speed, 0402+ chips)
      ↓
  Pick & Place #2 (large ICs, connectors, power components)
      ↓
  Pre-reflow AOI (optional intermediate check)
      ↓
  Reflow Oven (10-zone nitrogen atmosphere)
      ↓
  Post-reflow AOI
      ↓
  Wave Solder (through-hole components)
      ↓
  ICT (In-Circuit Test)
      ↓
  Depanelling
      ↓
  Boards to Inverter / SCC / UPS Assembly Lines
```

### 1.2 Equipment List — SMT Line

| # | Equipment | Model / Spec | Quantity | Key Parameters |
|---|---|---|---|---|
| SMT-01 | Solder Paste Printer | DEK Horizon 03iX or equivalent | 1 | ±12.5 µm repeatability; closed-loop squeegee pressure |
| SMT-02 | SPI (Solder Paste Inspection) | Koh Young Zenith or equivalent | 1 | 3D inspection; 100% measurement coverage |
| SMT-03 | Pick & Place — High Speed | Yamaha YSM20R or equivalent | 1 | 75,000 CPH; 0201 to 50×50 mm components |
| SMT-04 | Pick & Place — Flexible | Yamaha YSM10R or equivalent | 1 | 22,500 CPH; handles large power ICs, capacitors, transformers |
| SMT-05 | Reflow Oven | Heller 1964 MK5 or equivalent | 1 | 10 zones; nitrogen option; lead-free profile; max 350°C |
| SMT-06 | AOI (Post-reflow) | Koh Young Zenith 2 or equivalent | 1 | 3D AOI; <0.1% false-call rate target |
| SMT-07 | Wave Solder Machine | Rehm Versaflow 3/66 or equivalent | 1 | Dual-wave; lead-free solder; nitrogen option |
| SMT-08 | ICT (In-Circuit Tester) | Agilent/Keysight 3070 or equivalent | 1 | Bed-of-nails or flying probe; tests opens, shorts, component values |
| SMT-09 | Depanelling Router | LPKF MicroLine 2522 or equivalent | 1 | V-cut and routing; cleanroom-rated dust extraction |
| SMT-10 | Solder Paste Refrigerator | Dedicated 4°C unit | 1 | Stores solder paste; rotation-managed FIFO |
| SMT-11 | Reel Storage Cabinet | ESD-rated, climate-controlled | 2 | Component reels in moisture-barrier bags; tracked in MES |
| SMT-12 | ESD Workstation (rework) | Metcal MX-5200 or equivalent | 4 | BGA rework, component replacement, solder bridge repair |

**SMT Line Output Capacity:** ~3,000 PCB panels/day (two-shift operation), equivalent to
~18,000 individual inverter control boards/day at typical panel factor of 6.

---

## 2. Transformer & Inductor Winding Section

This is the **most labour-intensive and precision-demanding section of the factory** in Phase 1.
Transformer winding quality directly determines inverter efficiency, thermal performance, and
long-term reliability. Human winders operate toroidal and EI-core machines in Phase 1. CNC
winding automation is the single biggest Phase 2 productivity investment.

### 2.1 Winding Cell Layout

```
Raw Cores In-feed (from stores via AMR)
      ↓
  Toroidal Winding Machines (×2) ── Toroidal transformers for inverters
      ↓
  EI Core Winding Machines (×2) ── EI-core mains transformers + filter inductors
      ↓
  Bobbin Winders (×4) ── HF transformer bobbins for MPPT SCCs + chargers
      ↓
  Inductor Winders (×2) ── DC link chokes + EMI filter inductors
      ↓
  Varnish Tank (vacuum impregnation) ── Insulation + moisture protection
      ↓
  Transformer Tester (×2) ── Turns ratio, impedance, Hi-Pot, partial discharge
      ↓
  To Inverter / SCC / UPS Assembly Lines
```

### 2.2 Equipment List — Winding Section

| # | Equipment | Model / Spec | Quantity | Key Parameters |
|---|---|---|---|---|
| WND-01 | Toroidal Winding Machine | Meteor MT-2100 or equivalent | 2 | Up to 250 mm OD core; auto tension control; layer counting |
| WND-02 | EI Core Winding Machine | MARSILLI FH-300 or equivalent | 2 | EI-30 to EI-150 cores; up to 6-layer winding; auto wire guide |
| WND-03 | Bobbin Winder (HF) | Synthesis BWM-800 or equivalent | 4 | 50 Hz – 200 kHz range; 0.05 mm – 1.5 mm wire; multi-section |
| WND-04 | Inductor Winder | Gorman-Rupp / Custom CNC | 2 | Air-core and gapped-core inductors; ±5% tolerance |
| WND-05 | Vacuum Varnish Impregnation Tank | 80 L capacity; 30 mbar vacuum | 1 | Polyester/polyurethane varnish; 2-cycle vacuum-pressure process |
| WND-06 | Transformer Test Station | Hioki ST5510 or equivalent | 2 | Turns ratio, inductance, leakage inductance, DCR, Hi-Pot 3kVAC |
| WND-07 | Partial Discharge Tester | Doble M4000 or equivalent | 1 | IEC 60270 compliant; for high-power transformer validation |
| WND-08 | Wire Tension Meter | Checkline TL-200 or equivalent | 4 | Inline wire tension monitoring; alerts on ±10% deviation |
| WND-09 | Core Annealing Oven | Nabertherm N 7/H or equivalent | 1 | Stress relief anneal for cut toroidal cores; 400–700°C |

**Winding Section Output (Phase 1, Manual):**
- Toroidal transformers (1kVA–5kVA): ~120 units/day (2 machines × 2 shifts)
- EI-core transformers (500VA–2kVA): ~200 units/day
- HF transformer bobbins (SCCs, chargers): ~400 units/day
- Inductors: ~300 units/day

---

## 3. Inverter Assembly Line

The inverter assembly line integrates all sub-assemblies (wound transformer, SMT control PCB,
power stage PCB, harness, enclosure) into finished inverter units. Each unit is 100% load-bank
tested before packaging — no exceptions.

### 3.1 Line Configuration

```
Chassis Prep Station
  ↓ (AMR delivers enclosure from Coo-Cah Plastics store)
PCB Mount Station (power stage + control board)
  ↓
Transformer Integration Station (wound transformer installed, torqued)
  ↓
Wiring Harness & Terminal Assembly
  ↓
Firmware Flash Station (serial number, model code, FW version → MES)
  ↓
Pre-test Visual Inspection
  ↓
Load Bank Test Station (100% units — no skip)
  ↓
Final QC & Label Print-and-Apply (SON C-Mark, serial, QR code)
  ↓
Housing / Cover Install + Torque Check
  ↓
Packaging
```

### 3.2 Equipment List — Inverter Assembly Line

| # | Equipment | Model / Spec | Quantity | Key Parameters |
|---|---|---|---|---|
| INV-ASM-01 | Assembly Conveyor (powered) | 12 m × 600 mm belt; variable speed | 2 | 2 parallel lines; adjustable pallet carriers |
| INV-ASM-02 | Torque Screwdriver Set (ESD) | Desoutter LCV40 or equivalent | 12 | Traceable torque; records torque value per fastener in MES |
| INV-ASM-03 | Firmware Flash Station | Custom PC + J-Link/ST-Link; MES-integrated | 4 | Flashes MCU; records serial number, model, FW version |
| INV-ASM-04 | Cable Crimping Machine | Komax Gamma 333 or equivalent | 2 | Wire 0.5–6 mm²; crimps and tests pull-force inline |
| INV-ASM-05 | Harness Test Jig | Custom per SKU (6 jigs) | 6 | Tests wire continuity, correct pinout before harness install |
| INV-ASM-06 | Transformer Press-fit Jig | Custom per transformer size | 4 | Ensures consistent transformer seating and torque |
| INV-ASM-07 | BMS Programming Station | Custom PC + CAN interface | 2 | For inverter models with battery management integration |

---

## 4. Load Bank & Test Equipment

**POLICY: Every inverter, UPS, and solar charge controller is 100% tested on a load bank
before packaging. No unit ships without a passed test record in MES.**

This is the quality foundation of the factory and a core competitive differentiator: every
Coo-Cah inverter carries a load test certificate traceable to its serial number.

### 4.1 Equipment List — Test Zone

| # | Equipment | Model / Spec | Quantity | Key Parameters |
|---|---|---|---|---|
| TST-01 | Resistive Load Bank | Simplex / Crestchic 5 kW–50 kW programmable | 6 | For inverter and UPS load testing; 0–50 kW in 250 W steps |
| TST-02 | Power Quality Analyser | Fluke 435-II or equivalent | 4 | THD, PF, voltage, frequency, transient capture; IEC 61000 |
| TST-03 | Digital Storage Oscilloscope | Rigol DS1054Z / Tektronix TBS2000 | 6 | 100 MHz; 4 channels; for waveform capture during test |
| TST-04 | Battery Simulator | Chroma 17010 or equivalent | 4 | Simulates 12V / 24V / 48V battery; adjustable SOC profile |
| TST-05 | Hi-Pot (Hipot) Tester | Chroma 19030 or equivalent | 4 | AC + DC hipot; IEC 60335 / IEC 61010; records pass/fail in MES |
| TST-06 | Surge / Transient Generator | Haefely AXOS-8 or equivalent | 1 | IEC 61000-4-5 surge; 1.2/50 µs; up to 6 kV / 3 kA |
| TST-07 | EMC Pre-compliance Scanner | Rigol DSA815-TG + near-field probes | 1 | Conducted + radiated EMI pre-screening; 9 kHz – 1.5 GHz |
| TST-08 | SCC Test Bench | Custom: PV simulator + battery simulator + data logger | 3 | Tests MPPT tracking efficiency (≥ 97% target), PWM cycle, charge stages |
| TST-09 | UPS Transfer-Time Test Station | Custom: input switch + oscilloscope trigger | 2 | Measures transfer time to battery (< 4 ms for line-interactive) |
| TST-10 | Thermal Camera | FLIR E8-XT or equivalent | 2 | Infrared scan under full load; identifies hot spots before shipping |
| TST-11 | Multimeter / Clamp Meter (bench) | Keysight U1242C or equivalent | 20 | Standard bench measurement at all assembly and test stations |
| TST-12 | Environmental Chamber (small) | 50 L; -20°C to +85°C | 1 | Thermal cycling for accelerated reliability testing (sample basis) |
| TST-13 | LCR Meter | Keysight E4980A or equivalent | 2 | Measures L, C, R, ESR on capacitors and inductors during transformer test |

### 4.2 Load Bank Test Protocol Summary

| Product | Test Duration | Load Profile | Key Measurements |
|---|---|---|---|
| CCG-INV-PSW | 30 min at 100% rated load | Resistive + inductive mix | Output voltage, THD < 3%, frequency 50 Hz ± 0.5%, temperature |
| CCG-INV-MSW | 15 min at 100% rated load | Resistive | Output voltage (modified sine), no-load current, battery drain rate |
| CCG-SCC-MPPT | 20 min at rated PV + load | PV simulator + battery simulator | MPPT efficiency ≥ 97%, charge current accuracy ± 2%, heat |
| CCG-UPS | 30 min: mains + battery mode | Resistive; transfer-time test | Transfer < 4 ms, battery runtime at 100% load, output quality |
| CCG-BC | 60 min (full charge cycle) | Battery simulator | Stage transitions (bulk/absorption/float), accuracy, temperature |

---

## 5. Solar Charge Controller Assembly Line

Dedicated SCC line for MPPT and PWM controllers. Simpler assembly than inverters (no transformer
integration), but PCB quality and test rigour are equally critical.

| # | Equipment | Quantity | Key Parameters |
|---|---|---|---|
| SCC-ASM-01 | PCB Enclosure Assembly Jig | 4 | Positions PCB in SCC enclosure; guided screw torque |
| SCC-ASM-02 | Terminal Block Assembly Tool | 4 | Wire ferrule crimping + torque for PV and battery terminals |
| SCC-ASM-03 | Firmware Flash Station | 2 | Dedicated SCC firmware; records serial + MPPT algorithm version in MES |

---

## 6. Power Tool Assembly Line

Power tools (drills, angle grinders, circular saws) use a dedicated sub-assembly approach:
motor assembly, gearbox assembly, housing assembly, and final electrical test.

| # | Equipment | Quantity | Key Parameters |
|---|---|---|---|
| PT-ASM-01 | Motor Winding Inspection Station | 2 | Incoming QC on imported motor sub-assemblies (Johnson Electric / Mabuchi) |
| PT-ASM-02 | Gearbox Assembly Press | 2 | Bearing press-fit; gear mesh verification |
| PT-ASM-03 | Housing Assembly Conveyor | 1 | 8 m; 6 stations; poka-yoke guides for all variants |
| PT-ASM-04 | Power Tool Load Tester | 2 | No-load RPM, locked-rotor current, brush-down test |
| PT-ASM-05 | Hi-Pot Tester (tools) | 2 | IEC 60745-1; 1,000 V AC 1 min; class I tools |
| PT-ASM-06 | Torque Measurement Bench | 2 | Drill: torque at all clutch settings; Grinder: RPM under load |

---

## 7. Cable & Wire Processing

| # | Equipment | Quantity | Key Parameters |
|---|---|---|---|
| CBL-01 | Wire Cutting & Stripping Machine | Komax Zeta 633 or equivalent | 2 | AWG 20 – 4; cut length ±0.5 mm; strip length ±0.3 mm |
| CBL-02 | Ferrule Crimping Machine | Weidmüller CRIMPFIX or equivalent | 4 | For ferrule crimping on all control wires |
| CBL-03 | Lug / Terminal Crimper (hydraulic) | Mecal MP60T or equivalent | 2 | 6 mm² – 120 mm² power cables; battery cables |
| CBL-04 | Wire Marker Printer | Brady BBP31 or equivalent | 2 | Heat-shrink tube labels; traces all harness wires by MES serial |
| CBL-05 | Continuity Tester (harness) | Custom 64-point test fixture × 6 | 6 | Tests each cable harness before installation |

---

## 8. AMR Fleet (Autonomous Mobile Robots)

The AMR fleet handles kitting, WIP transport between zones, and finished goods movement
to the packaging and warehouse areas. This eliminates manual forklift movement within the
production floor and reduces material handling errors.

| # | Equipment | Model / Spec | Quantity | Key Parameters |
|---|---|---|---|---|
| AMR-01 | Autonomous Mobile Robot | Geek+ P40 or equivalent | 12 | 1,000 kg payload; 1.5 m/s; LiDAR + vision navigation |
| AMR-02 | AMR Charging Stations | Compatible with Geek+ P40 | 4 | Opportunity-charging during queue wait; 80% charge in 45 min |
| AMR-03 | AMR Fleet Management System | Geek+ RCS (Robot Control System) | 1 (software) | MES-integrated; WIP order tracking; zone traffic management |

**AMR Zone Assignments:**
- Stores → SMT in-feed: component kits on ESD trays
- Winding cell → Inverter assembly: wound transformers on padded carriers
- SMT out-feed → Inverter / SCC / UPS assembly: PCB trays
- Inverter assembly → Load bank test queue
- Load bank → Packaging
- Packaging → Finished goods warehouse

---

## 9. Packaging Line

| # | Equipment | Quantity | Key Parameters |
|---|---|---|---|
| PKG-01 | Carton Erector | 1 | Auto-erects inverter / UPS / SCC cartons; 15 cartons/min |
| PKG-02 | Auto-taper / Case Sealer | 2 | Top and bottom tape seal |
| PKG-03 | Label Print-and-Apply System | 2 | MES-triggered; prints SON C-Mark label, serial QR code, NCC label |
| PKG-04 | Check-weigher | 1 | Rejects over/underweight cartons; detects missing accessories |
| PKG-05 | Stretch Wrap Machine | 1 | Pallet wrapping for finished goods |
| PKG-06 | Thermal Transfer Printer (label) | Brady BMP71 or equivalent | 4 | Backup manual label printing |

---

## 10. Energy Systems

| # | Equipment | Spec | Quantity | Notes |
|---|---|---|---|---|
| ENE-01 | Ground-Mount Solar Array | 600 kWp; monocrystalline PERC | 1 array | ~1,500 panels × 400W; east of factory building + car park canopy |
| ENE-02 | String Inverter (solar) | Huawei SUN2000-100KTL or equivalent | 6 × 100 kW | Grid-forming mode; supports island operation with BESS |
| ENE-03 | BESS (Battery Energy Storage) | 700 kWh LFP; CATL or BYD containerised | 1 × 700 kWh | 20-year calendar life; BMS with remote monitoring |
| ENE-04 | ATS (Automatic Transfer Switch) | 630 A; <500 ms transfer | 1 | Switches between grid / solar+BESS / generator automatically |
| ENE-05 | Backup Generator | Perkins 400 kVA diesel; Stamford alternator | 1 | 1,500 L fuel tank; ~60 h runtime at 40% load; auto-start on ATS |
| ENE-06 | Power Factor Correction Bank | 200 kVAr automatic PFC | 1 | Maintains PF > 0.95 on DISCO supply billing meter |
| ENE-07 | Energy Monitoring System | Schneider EcoStruxure Power Monitoring Expert | 1 | All distribution boards submetered; data fed to digital twin |

---

## 11. Facility Support Equipment

| # | Equipment | Quantity | Notes |
|---|---|---|---|
| FAC-01 | ESD Flooring (production zones) | ~5,500 m² | Conductive epoxy; IEC 61340-5-1 compliant; monthly resistance test |
| FAC-02 | Compressed Air System | 110 kW screw compressor; 500 L receiver; desiccant dryer | 1 | 7 bar; dewpoint -40°C; feeds SMT, winding, assembly |
| FAC-03 | Fume Extraction (soldering) | Integrated with SMT line + rework stations | Central + local | Solder fume below WEL per COSHH |
| FAC-04 | ESD Wrist Strap Tester | 20 | At every ESD-sensitive workstation |
| FAC-05 | Calibration Standards Set | Traceable to NAFDAC/NIS | Per lab | Annual recalibration; records in MES |
| FAC-06 | Overhead Cranes | 2-ton capacity | 2 | For transformer and generator handling |

---

## Equipment Procurement Schedule (Phase 1)

| Batch | Equipment Group | Target Delivery | Budget (USD) |
|---|---|---|---|
| Batch 1 | SMT line (full) | Q1 2026 | ~$850,000 |
| Batch 2 | Winding machines + varnish tank | Q1 2026 | ~$180,000 |
| Batch 3 | Load bank + test equipment | Q2 2026 | ~$220,000 |
| Batch 4 | Assembly conveyors + tools | Q1 2026 | ~$90,000 |
| Batch 5 | AMR fleet (12 units) | Q2 2026 | ~$310,000 |
| Batch 6 | Packaging line | Q2 2026 | ~$75,000 |
| Batch 7 | Energy systems (solar + BESS + generator) | Q1–Q2 2026 | ~$1,200,000 |
| **Total Phase 1 Equipment** | | | **~$2,925,000** |

> All USD estimates at 2025 pricing. Final procurement in USD or EUR; Nigerian Naira
> conversion at prevailing CBN rate at time of Form M submission.
