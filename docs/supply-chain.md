# Supply Chain Strategy

**Factory:** Coo-Cah Garage & Power Electronics Factory, Sagamu, Ogun State
**Document Ref:** CCG-PE-SCHN-001 | **Version:** 1.0

> This document follows the Coo-Cah group supply chain doctrine defined in
> `docs/supply-chain/doctrine.md` within [Coo-Kah-Doks](https://github.com/oumar-code/Coo-Kah-Doks).

---

## 1. Semiconductor Supply Chain Strategy

### 1.1 Why Semiconductors Are the Highest-Risk Component

Power electronics are fundamentally semiconductor-constrained. Every Coo-Cah inverter contains:
- 8–24 power MOSFETs or IGBTs (switching elements in the inverter bridge)
- 2–4 gate driver ICs per bridge
- 1–2 microcontrollers (MCU) — main control + auxiliary

These components are:
1. **Safety-critical** — a substandard MOSFET can cause thermal runaway, fire, or explosion.
2. **Allocation-controlled** — Infineon, ON Semiconductor, and TI allocate based on forecast
   commitments. A factory without a purchase order history will be deprioritised.
3. **Counterfeit-prone** — the Nigerian electronics market has significant counterfeit
   semiconductor problems. Coo-Cah's quality reputation depends on sourcing only genuine parts.
4. **Long lead time** — genuine distributor lead times for popular power MOSFETs can be
   16–52 weeks. The semiconductor shortage of 2021–2023 demonstrated this catastrophically.

### 1.2 Semiconductor Procurement Policy

| Policy | Requirement |
|---|---|
| **Source** | Authorised distributors ONLY — Arrow Electronics, Avnet, Mouser, Digi-Key |
| **Counterfeit prevention** | 100% of semiconductors verified via manufacturer CoC (Certificate of Conformance) + incoming inspection (IPC-A-600); random sample testing on LCR meter / curve tracer |
| **Safety stock** | **90 days minimum** at all times (see rationale below) |
| **Dual source** | Every critical semiconductor must have a qualified second source |
| **Shipping mode** | **Air freight only** — no sea freight for semiconductors |
| **Import compliance** | Form M + SON CoC for every shipment |
| **Currency** | USD; hedging via CBN forward contracts for large purchases |
| **Supplier audit** | Annual visit or virtual audit of primary distributor warehouse |

### 1.3 Why 90-Day Safety Stock for Semiconductors

```
Normal distributor lead time (authorised channel): 8–16 weeks
Shortage period lead time (2021–2023 precedent):   52+ weeks
Nigeria customs clearance:                          2–5 days (air freight)
Air freight transit time (Europe/USA to Lagos):     2–5 days
                                                   ─────────────────
Worst-case total replenishment time:               ~57 weeks (shortage scenario)
```

**90 days (3 months) of safety stock is therefore the minimum defensible position.** Even
with 90 days on-hand, a sudden allocation cut or shipping disruption creates risk. The Phase 2
target is 120 days for MOSFETs and IGBTs specifically.

### 1.4 Primary Semiconductor Suppliers

| Component | Primary Supplier | Part Examples | Alt Source | Shipping |
|---|---|---|---|---|
| Power MOSFETs (600V N-ch) | Infineon Technologies (Germany) | IPW60R070CFD7, IPW65R190CFD | ON Semiconductor | Air freight |
| Power MOSFETs (200V N-ch) | Infineon Technologies | IPB200N25N3 G | STMicroelectronics | Air freight |
| IGBTs (600V for UPS) | Infineon Technologies | IKW40N120H3 | ON Semiconductor | Air freight |
| Gate Driver ICs | Texas Instruments (USA) | UCC27714, ISO5852S | Microchip Technology | Air freight |
| Microcontrollers (inverter) | STMicroelectronics | STM32G474RE | NXP, Renesas | Air freight |
| MCU (SCC, charger) | Microchip Technology | dsPIC33CK256MP506 | STMicro | Air freight |
| Hall Effect current sensors | Allegro MicroSystems | ACS770 series | Honeywell | Air freight |
| Op-amps / comparators | Texas Instruments | TL431, LM393 | ON Semiconductor | Air/Sea |
| Wi-Fi MCU (CCG-PS strips) | Espressif Systems | ESP32-S3 | — | Air freight |

### 1.5 Safety Stock Policy Table

| Component Category | Safety Stock | Shipping Mode | Primary Risk | Lead Time |
|---|---|---|---|---|
| Power MOSFETs / IGBTs | **90 days** | Air freight only | Allocation cuts; counterfeits | 8–16 weeks normal |
| Gate Driver ICs | **90 days** | Air freight only | Allocation cuts | 8–12 weeks normal |
| Microcontrollers | **90 days** | Air freight only | Allocation; EOL risk | 10–16 weeks normal |
| Toroidal / EI transformer cores | **60 days** | Sea freight (Tin Can Island) | Sea freight delays | 22–28 days transit |
| Magnet wire (copper) | **21 days** | Local / import mix | Local supply reliable | 3–7 days local |
| Electrolytic capacitors (critical) | **45 days** | Air freight (critical grades) | Japanese fab capacity | 8–12 weeks |
| Electrolytic capacitors (standard) | **30 days** | Sea freight | Lower risk | 4–6 weeks |
| PCB bare boards | **30 days** | LCL sea freight | China/Taiwan lead times | 4–6 weeks |
| Plastic enclosures (Coo-Cah Plastics) | **7 days** | Intra-group daily delivery | Intra-group reliability | 1–2 days |
| UPS VRLA batteries | **30 days** | Sea freight (DG) | DG shipping constraints | 4–6 weeks |
| Solar panels (CCG-SPK kits) | **45 days** | Sea freight | Port congestion | 4–6 weeks |
| Power tool motors | **60 days** | Sea freight | OEM lead times | 5–8 weeks |
| Power tool gearboxes | **60 days** | Sea freight | OEM lead times | 5–8 weeks |

---

## 2. Intra-Group Supply — Coo-Cah Plastics & Polymers Factory

### 2.1 Strategic Importance

Plastic enclosures are the second most visible quality indicator after electrical performance.
The Coo-Cah Plastics & Polymers Factory in Agbara, Lagos, is the **Tier A strategic supplier**
for all plastic parts. This intra-group relationship is fundamental to the supply chain strategy:

| Benefit | Value |
|---|---|
| Lead time | 1–2 days (60 km by road on Coo-Cah logistics fleet — daily delivery) |
| Safety stock needed | Only 7 days (vs. 30–45 days for external supplier) |
| Quality control | Shared quality standards; no incoming inspection delay |
| Design collaboration | Enclosure designs co-developed; DFM feedback loops within the group |
| Cost | Intra-group transfer pricing; no import duties, no forex risk |
| Flexibility | Priority allocation for Coo-Cah electronics vs. commercial orders |

### 2.2 Enclosure Specification Table

| Product | Part Description | Material | Colour | Key Dimensions |
|---|---|---|---|---|
| CCG-INV-PSW 300VA–1kVA | Small inverter housing (top + bottom shell) | ABS (UL94 V-0) | RAL 7016 Anthracite | 240×130×100 mm |
| CCG-INV-PSW 2kVA–3kVA | Medium inverter housing | ABS (UL94 V-0) | RAL 7016 | 340×180×120 mm |
| CCG-INV-PSW 5kVA | Large inverter housing | ABS + steel chassis insert | RAL 7016 | 420×220×150 mm |
| CCG-SCC-MPPT (all) | SCC enclosure (IP20) | ABS (UL94 V-0) | RAL 7035 Light Grey | 200×120×60 mm |
| CCG-PS 4-way | Power strip body + top cover | PC/ABS (UL94 V-0) | White / Black | 330×50×35 mm |
| CCG-PS 6-way | Power strip body + top cover | PC/ABS (UL94 V-0) | White / Black | 460×50×35 mm |
| CCG-PS 8-way | Power strip body + top cover | PC/ABS (UL94 V-0) | White / Black | 580×50×35 mm |
| CCG-UPS 600VA–1kVA | UPS housing | ABS (UL94 V-0) | RAL 7016 | 300×200×130 mm |
| CCG-BC (all) | Charger enclosure | ABS (UL94 V-0) | RAL 7016 | 220×130×80 mm |

> **Contingency:** If Coo-Cah Plastics is not yet operational at factory launch, interim supply
> from Lagos-based injection moulders (e.g., Polylastic Nigeria, Bel Papyrus Group plastics arm)
> using Coo-Cah-provided tooling. Mould tools are owned by Coo-Cah Electronics, not the supplier.

### 2.3 Daily Delivery Schedule

- **06:00** — Outgoing order placed by MES (based on previous day's production + safety stock delta)
- **09:00** — Coo-Cah logistics truck departs Agbara
- **11:30** — Delivery to Sagamu factory loading bay (±30 min Sagamu–Agbara road conditions)
- **12:00** — Incoming count and quality spot-check; AMR loads to Zone I stores
- **14:00** — Next-day order confirmed with Coo-Cah Plastics production team via group ERP

---

## 3. Transformer Core Import Strategy

### 3.1 Phase 1 — Import from China

| Parameter | Value |
|---|---|
| Supplier | Baoding Tianwei Group / Zhejiang Yongda Electronics / equivalent Chinese transformer core manufacturer |
| Core Types | Toroidal cores (silicon steel tape-wound): 100VA–5kVA range; EI lamination stacks: EI-48 to EI-150 |
| Material | Cold-rolled grain-oriented silicon steel (CRGO); M4/M5 grade |
| Port | Tin Can Island Port, Lagos (nearest container terminal to Sagamu) |
| Freight Mode | FCL / LCL sea freight from Tianjin/Shanghai |
| Transit Time | 22–28 days sea + 5–10 days customs clearance = ~32–38 days total |
| Safety Stock | 60 days |
| Annual Volume | ~500,000 toroidal cores + ~300,000 EI lamination stacks (Phase 1) |

### 3.2 Phase 2 — Local Sourcing Investigation

In Phase 2 (2027–2028), the supply chain team will investigate:
1. **Coo-Cah Metallurgical Factory** — potential to produce silicon steel laminations locally.
   This would be a group-strategic win: local transformer core supply eliminates sea freight
   lead times and forex exposure on one of the heaviest components.
2. **Nigerian steel laminators** — NNPC-linked steel processing, Delta Steel Company, or similar.
3. **Decision criteria:** Quality conformance to IEC 60404 (magnetic core material standard);
   price within 15% of Chinese import; supply reliability ≥ 95% on-time.

---

## 4. Magnet Wire (Copper Winding Wire)

| Specification | Requirement |
|---|---|
| Material | 99.9% electrolytic tough pitch copper (ETP) |
| Insulation | Grade 2 polyurethane (180°C thermal class) or polyester-imide |
| Standard | IEC 60317-2 (polyurethane) / IEC 60317-8 (polyester-imide) |
| Gauge Range | AWG 38 (0.1 mm) to AWG 10 (2.6 mm) — multiple gauges on-site |

| Supplier | Type | Gauge Range | Lead Time | Annual Volume |
|---|---|---|---|---|
| Kabelmetal Nigeria Ltd (Lagos) | Local manufacturer | 0.5–2.0 mm common gauges | 3–7 days | ~60 tonnes/year |
| Nigerchin / BCC Cables (Lagos) | Local manufacturer | 0.5–1.5 mm | 3–7 days | Backup to Kabelmetal |
| Indian Import (Superstar / Precision) | Import via sea | 0.1–0.5 mm (fine wire, HF bobbins) | 14–21 days | ~15 tonnes/year |

**Strategy:** Maximise local sourcing (Lagos-based) for common gauges to minimise forex exposure
and lead times. Import only specialist fine gauges where local supply quality is insufficient.

---

## 5. Electrolytic Capacitors

| Grade | Supplier | Shipping | Safety Stock | Use Case |
|---|---|---|---|---|
| High-reliability (105°C, long-life) | Nichicon (Japan), Rubycon (Japan) | **Air freight** | 45 days | Inverter DC bus caps; UPS backup caps |
| Standard (85°C) | Lelon (Taiwan), Su'scon (Taiwan) | Sea freight | 30 days | SCC, charger, power strip |
| High-voltage (450V+) | United Chemi-Con (Japan) | Air freight | 45 days | Inverter PFC stage |

**Key concern:** Japanese capacitor manufacturers (Nichicon, Rubycon) have long lead times
(12–16 weeks) for allocated grades. Building 45-day safety stock is the minimum defensible
buffer. Phase 2 target: qualify ELNA or Samwha (Korean) as a second source for critical grades.

---

## 6. UPS Battery (VRLA) — Hazardous Goods Logistics

### 6.1 Classification

| Parameter | Value |
|---|---|
| Battery Type | Valve Regulated Lead Acid (VRLA / SLA) |
| UN Number | UN 2800 (non-spillable); UN 2794 (wet) |
| IMDG Class | Class 8 — Corrosive; Packing Group III |
| ADR/RID Class (road/rail) | Class 8 |
| Air freight (IATA DGR) | **PROHIBITED in cargo aircraft** for some configurations; consult DG specialist |

### 6.2 Logistics Requirements

| Requirement | Detail |
|---|---|
| Shipping mode | **Sea freight only** (IMDG Class 8 compliant) |
| Carrier requirements | DG-certified container line; DG declaration (IMO 4.1 Dangerous Goods Form) |
| Packaging | UN-certified packaging; each battery in individual polyethylene bag; terminal protection |
| Forwarder | Must hold IATA/FIATA DG licence; DG specialist required |
| Customs | SON CoC required for batteries; NESREA import permit (hazardous material) |
| Storage at factory | Dedicated DG cage (Zone I stores); ventilated; segregated from flammables |
| Disposal | Licensed NESREA-registered battery recycler; annual disposal report to NESREA |

### 6.3 Phase 2 Battery Strategy

In Phase 2 (2027–2028), evaluate switching UPS backup batteries from VRLA to **LiFePO₄ packs**
assembled by the Coo-Cah BESS Assembly Line. Benefits:
- Eliminates DG shipping (LiFePO₄ cells are not IMDG Class 8)
- Reduces battery volume and weight in UPS units
- Aligns with Coo-Cah's group-wide LiFePO₄ strategy
- Intra-group supply (no forex, no customs, 1–2 day lead time)

---

## 7. Intra-Group Supply — What This Factory Delivers to Sister Factories

This factory is a **supplier** to every other Coo-Cah factory. Internal allocation has priority
over commercial sales.

| Recipient Factory | Product | Estimated Annual Volume | Delivery Schedule |
|---|---|---|---|
| All Coo-Cah factories (every site) | CCG-INV-PSW 3kVA (backup power) | ~500 units total (one per critical circuit) | One-time fit-out; then replacement on failure |
| All Coo-Cah factories (every site) | CCG-INV-PSW 5kVA (large loads) | ~200 units total | One-time fit-out |
| All Coo-Cah factories (IT rooms) | CCG-UPS 1kVA rack-mount | ~1,200 units (6 per factory × 200 factories-equiv) | Ongoing; 2-year refresh cycle |
| All Coo-Cah factories (workstations) | CCG-PS 6-way Smart Power Strip | ~50,000 units/year | Monthly delivery on Coo-Cah logistics |
| Coo-Cah Energy Team (solar installs) | CCG-SCC-MPPT 40A + 60A | ~10,000 units/year | Per project schedule |
| All factory maintenance workshops | CCG-PT-DRILL + CCG-PT-AG | ~2,000 units/year | Quarterly replenishment |

**Internal allocation protocol:**
1. MES generates intra-group supply orders from group ERP (Coo-Kah-Doks orchestration)
2. Internal orders are picked before commercial orders in the same production batch
3. Internal pricing: cost-plus 10% (no commercial margin; group internal transfer price)
4. Commercial sales begin when Phase 1 production capacity exceeds internal demand

---

## 8. Nigerian Market Opportunity

### 8.1 Market Size & Growth

| Metric | Value | Source |
|---|---|---|
| Nigeria inverter market size (2024) | ~2.1 million units/year | Industry estimates; NEMSA data |
| Annual growth rate | 15–20% | Driven by DISCO grid deterioration |
| Annual market value (2024) | ~₦480 billion (~USD 620M) | Blended ASP ~₦230,000/unit |
| Addressable segment (mid-market) | ~800,000 units/year | Excluding low-end modified sine |
| MPPT solar controller market | ~600,000 units/year | Growing with rooftop solar adoption |
| Smart power strip market | ~1.5 million units/year | Every household and business |

### 8.2 Competitive Positioning

| Factor | Coo-Cah Advantage | Competition (Imported Chinese brands) |
|---|---|---|
| **Local warranty** | 2-year warranty; factory-direct service in Sagamu | Typically 6-month warranty; no local service |
| **SON certification** | NIS-certified — legally required in Nigeria | Many imports not SON-certified (grey market) |
| **Price** | Mid-market; ~15% premium vs. grey-market imports | Grey imports cheaper but no warranty/cert |
| **Lead time (restocking)** | Same-day for Lagos; next-day for other states | 4–8 weeks (sea freight from China) |
| **Brand** | Nigerian-made; Coo-Cah brand trust via other products | Foreign brands; no local relationship |
| **Service** | Sagamu aftersales centre; Lagos service agents | No local authorised service |

### 8.3 Revenue Ramp Model

| Year | Internal Sales | External B2B | External Retail | Total Revenue (₦B) |
|---|---|---|---|---|
| 2027 (Year 1 commercial) | ₦2.1B | ₦4.5B | ₦1.2B | **₦7.8B** |
| 2028 (Year 2) | ₦2.3B | ₦12B | ₦5.5B | **₦19.8B** |
| 2029 (Phase 3 start) | ₦2.5B | ₦28B | ₦15B | **₦45.5B** |
| 2031 (Phase 3 full) | ₦3B | ₦65B | ₦40B | **₦108B** |

> Revenue model assumes: ASP growth of ~8%/year (Nigeria inflation adjustment);
> market share capture of ~5% of addressable mid-market by 2031.

### 8.4 B2B Sales Channels

| Channel | Target Customer | Product Focus |
|---|---|---|
| Direct enterprise sales | Telecoms (MTN, Airtel — BTS backup power) | 3kVA–5kVA PSW inverters |
| Industrial distributors | Manufacturing companies; hotels; hospitals | 2kVA–5kVA inverters; UPS |
| Solar installers | Residential and commercial solar project companies | MPPT SCCs; inverters |
| IT/telecoms distributors | Retail electronics stores; IT resellers | Smart power strips; UPS |
| E-commerce | Jumia, Konga — direct B2C | Power strips; 300VA–1kVA inverters |
