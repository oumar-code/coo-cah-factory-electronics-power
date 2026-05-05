# CapEx / OpEx Financial Model

**Factory:** Coo-Cah Garage & Power Electronics Factory, Sagamu, Ogun State
**Document Ref:** CCG-PE-FINC-001 | **Version:** 1.0

> All financial figures are estimates for planning purposes. Values in Nigerian Naira (₦)
> use an exchange rate of USD 1 = ₦775 (2025 planning rate). Naira figures reflect
> Nigeria's current tariff and operating cost environment.

---

## 1. Phased Capital Expenditure (CapEx)

### 1.1 Phase 1 CapEx Summary (2025–2026)

| Category | Item | USD Estimate | ₦ Equivalent |
|---|---|---|---|
| **Land & Site** | Site lease (5-year prepaid + security deposit) | $180,000 | ₦139.5M |
| **Civil & Construction** | Main factory building (~8,000 m²) | $1,600,000 | ₦1,240M |
| | Office & welfare block (~600 m²) | $180,000 | ₦139.5M |
| | Generator house + fuel tank (buried) | $45,000 | ₦34.9M |
| | Loading bay + dock levellers (4 doors) | $60,000 | ₦46.5M |
| | Site roads, drainage, perimeter wall, gate | $120,000 | ₦93M |
| | ESD flooring (production zones) | $85,000 | ₦65.9M |
| **Energy Systems** | 600 kWp ground-mount solar + car park canopy | $620,000 | ₦480.5M |
| | 700 kWh LFP BESS (2 × 350 kWh containers) | $385,000 | ₦298.4M |
| | 400 kVA Perkins generator + acoustic enclosure | $95,000 | ₦73.6M |
| | ATS + PFC bank + electrical distribution | $100,000 | ₦77.5M |
| **Production Equipment** | SMT line (full — see machinery.md) | $850,000 | ₦658.8M |
| | Transformer winding machines + varnish tank | $180,000 | ₦139.5M |
| | Load bank + test equipment | $220,000 | ₦170.5M |
| | Inverter assembly line conveyors + tools | $90,000 | ₦69.8M |
| | Power tool assembly line | $55,000 | ₦42.6M |
| | Cable and wire processing equipment | $35,000 | ₦27.1M |
| | SCC / UPS assembly benches + jigs | $40,000 | ₦31M |
| | Packaging line | $75,000 | ₦58.1M |
| **AMR Fleet** | 12 × Geek+ P40 AMR + charging stations + RCS | $310,000 | ₦240.3M |
| **IT / MES / Network** | MES software licences (3-year) | $120,000 | ₦93M |
| | Server hardware + networking | $85,000 | ₦65.9M |
| | Factory Wi-Fi 6 + OT network | $30,000 | ₦23.3M |
| | CCTV + access control | $25,000 | ₦19.4M |
| **Tooling & Jigs** | PCB test fixtures (× 6 SKUs) | $45,000 | ₦34.9M |
| | Enclosure assembly jigs (× all SKUs) | $30,000 | ₦23.3M |
| | Firmware flash station × 6 | $18,000 | ₦14M |
| **Quality & Lab** | Calibration standards set | $15,000 | ₦11.6M |
| | Thermal camera × 2 | $8,000 | ₦6.2M |
| | EMC pre-compliance scanner | $12,000 | ₦9.3M |
| **Regulatory & Legal** | SON NIS type-test fees (all Phase 1 SKUs) | $35,000 | ₦27.1M |
| | NCC Type Approval (CCG-PS + Wi-Fi models) | $18,000 | ₦14M |
| | NESREA EIA + permits | $20,000 | ₦15.5M |
| | NIPC Pioneer Status application | $12,000 | ₦9.3M |
| | ISO 9001 + ISO 45001 certification | $22,000 | ₦17.1M |
| | Legal (contracts, IP, land) | $40,000 | ₦31M |
| **Working Capital (6 months)** | Initial component inventory (90-day safety stock) | $850,000 | ₦658.8M |
| | Initial magnet wire + cores + plastics inventory | $180,000 | ₦139.5M |
| | Staff ramp-up costs (3 months training before production) | $200,000 | ₦155M |
| **Contingency** | 10% on construction + equipment | $385,000 | ₦298.4M |
| **TOTAL PHASE 1 CAPEX** | | **$6,625,000** | **₦5,134M (~₦5.1 billion)** |

### 1.2 Phase 2 CapEx Summary (2027–2028)

| Category | USD Estimate | ₦ Equivalent (2027 rate est.) |
|---|---|---|
| CNC transformer winding machines (6 units) | $620,000 | ₦620M |
| Phase 2 building extension (~2,000 m² CNC hall) | $480,000 | ₦480M |
| AI Vision QC upgrade (SMT AOI AI module) | $85,000 | ₦85M |
| Digital twin platform (Phase 2 live) | $120,000 | ₦120M |
| Additional load bank capacity | $65,000 | ₦65M |
| Additional SMT reels + feeders | $45,000 | ₦45M |
| Working capital increase | $380,000 | ₦380M |
| **TOTAL PHASE 2 CAPEX** | **$1,795,000** | **~₦1.8 billion** |

### 1.3 Phase 3 CapEx Summary (2029–2031)

| Category | USD Estimate | ₦ Equivalent (2030 rate est.) |
|---|---|---|
| Lights-out assembly block (~2,000 m²) | $720,000 | ₦900M |
| Automated power strip assembly line (lights-out) | $380,000 | ₦475M |
| AI failure diagnostics platform | $95,000 | ₦119M |
| Additional solar (200 kWp) + BESS expansion | $280,000 | ₦350M |
| SMT line 2 (second SMT line for 1.5M power strips) | $650,000 | ₦813M |
| Working capital increase | $500,000 | ₦625M |
| **TOTAL PHASE 3 CAPEX** | **$2,625,000** | **~₦3.3 billion** |

---

## 2. Unit Economics — Inverter BOM Cost Model

### 2.1 CCG-INV-PSW 2kVA — Detailed BOM Cost

| Component Category | Key Components | Unit Cost (₦) | Notes |
|---|---|---|---|
| Power MOSFETs (× 8) | Infineon IPW60R070CFD7 | ₦18,400 | 8 × ₦2,300; air freight included |
| Gate driver ICs (× 4) | TI UCC27714 | ₦4,800 | 4 × ₦1,200 |
| Microcontroller | STM32G474RE | ₦3,200 | 1 unit |
| Toroidal transformer (2kVA) | Core + winding (in-house) | ₦14,500 | Core ₦5,500 import; winding labour ₦9,000 |
| Electrolytic capacitors | DC bus 450V 4700µF × 2 (Nichicon) | ₦9,600 | Critical grade; air freight |
| Filter inductors (in-house wound) | Core + wire + labour | ₦3,800 | |
| Miscellaneous capacitors + resistors | Leaded + SMT passives | ₦2,200 | |
| PCB (control + power stage) | 2 bare boards + SMT assembly | ₦6,500 | In-house SMT; board import ₦3,500 |
| Plastic enclosure | From Coo-Cah Plastics | ₦4,800 | Intra-group transfer price |
| Display (LCD + buttons) | 2×16 LCD + keypad | ₦1,800 | |
| Battery terminals + connectors | Anderson + ring terminals | ₦1,200 | |
| Wiring harness (in-house) | 1 m² wire + ferrules + labels | ₦2,400 | |
| Cooling fan | 80 mm 12V DC brushless | ₦800 | |
| Firmware (flash at station) | Internal cost only | ₦0 | Amortised in software cost |
| Packaging (carton + accessories) | Carton + manual + cables | ₦1,500 | |
| **Total Direct Materials** | | **₦75,500** | |
| Direct Labour (assembly + test) | 45 min assembly + 30 min load bank test | ₦4,200 | At ₦5,600/hr blended rate |
| **Cost of Goods Manufactured (COGM)** | | **₦79,700** | |
| Manufacturing overhead (35% of DL) | Energy, depreciation, maintenance | ₦1,470 | |
| **Total Manufacturing Cost** | | **₦81,170** | |
| **SG&A + Distribution (15%)** | | ₦12,176 | |
| **Total Cost per Unit** | | **~₦93,350** | |

### 2.2 CCG-INV-PSW 2kVA — Price and Margin Model

| Channel | Selling Price | Gross Margin | Net Margin |
|---|---|---|---|
| Internal (sister factories) | ₦89,000 (cost + 10%) | 8% | 3% |
| B2B wholesale (distributors) | ₦165,000 | 44% | 34% |
| B2B direct (enterprise) | ₦185,000 | 49% | 39% |
| Retail (Jumia / Konga) | ₦210,000 | 55% | 43% |
| **Chinese import equivalent (grey market)** | **~₦130,000** | — | — |

> Coo-Cah's 2kVA PSW inverter at ₦165,000 (B2B) vs. ₦130,000 (unbranded Chinese grey market)
> carries a 27% premium. This is justified by: 2-year local warranty, SON certification,
> Coo-Cah brand, and local aftersales support. Customer surveys in the Nigerian market confirm
> that buyers at this segment strongly prefer local warranty support.

### 2.3 Unit Economics — Other Key Products

| Product | BOM Cost | COGM | B2B Price | Gross Margin |
|---|---|---|---|---|
| CCG-INV-PSW 3kVA | ₦108,000 | ₦116,500 | ₦235,000 | 50% |
| CCG-INV-PSW 5kVA | ₦165,000 | ₦178,000 | ₦380,000 | 53% |
| CCG-SCC-MPPT 40A | ₦28,500 | ₦31,200 | ₦62,000 | 50% |
| CCG-SCC-MPPT 60A | ₦38,000 | ₦41,500 | ₦82,000 | 49% |
| CCG-PS 6-way Smart Strip | ₦8,200 | ₦9,100 | ₦22,500 | 60% |
| CCG-UPS 1kVA | ₦65,000 | ₦71,000 | ₦145,000 | 51% |
| CCG-PT-DRILL 500W | ₦18,500 | ₦20,800 | ₦45,000 | 54% |

---

## 3. Operating Expenditure (Annual OpEx)

### 3.1 Phase 1 Annual OpEx (from Year 1 of Production — 2027)

| Category | Annual (₦M) | Notes |
|---|---|---|
| **Labour** | | |
| Production staff (280 direct × ₦840,000/year avg) | ₦235.2M | Avg ₦70,000/month blended all grades |
| Indirect staff (60 × ₦720,000/year avg) | ₦43.2M | Security, logistics, admin |
| Management + engineering (20 × ₦2.4M/year avg) | ₦48M | |
| **Labour Total** | **₦326.4M** | |
| **Energy** | | |
| Grid electricity (residual ~145,000 kWh × ₦215) | ₦31.2M | With solar + BESS |
| Generator diesel (estimated 200h × 60L × ₦1,250) | ₦15M | Emergency backup only |
| **Energy Total** | **₦46.2M** | |
| **Materials & Components** | Covered in COGM (above) | — |
| **Maintenance** | | |
| SMT line + equipment maintenance contracts | ₦28M | ~3% of equipment CapEx |
| AMR fleet maintenance | ₦8M | Geek+ annual service contract |
| Building + facility maintenance | ₦12M | |
| **Maintenance Total** | **₦48M** | |
| **Regulatory & Compliance** | | |
| Annual SON surveillance audits | ₦4M | Per-certificate fees |
| ISO 9001 + 45001 annual surveillance | ₦3.5M | |
| NESREA annual reports + e-waste management | ₦2M | |
| NCC Type Approval renewals | ₦1M | |
| **Regulatory Total** | **₦10.5M** | |
| **SG&A** | | |
| Commercial team (sales + marketing) | ₦35M | |
| Finance + legal + HR | ₦20M | |
| Marketing + brand | ₦15M | |
| **SG&A Total** | **₦70M** | |
| **Finance Costs** | | |
| Loan servicing (if project financed) | ₦85M | Estimate at 18% p.a. on ₦2B loan |
| **TOTAL ANNUAL OPEX (Phase 1)** | **~₦586M** | |

---

## 4. Financial Performance Projections

### 4.1 Revenue and EBITDA

| Year | Revenue (₦B) | COGM (₦B) | Gross Profit (₦B) | OpEx (₦B) | EBITDA (₦B) | EBITDA % |
|---|---|---|---|---|---|---|
| 2027 (Yr 1) | 7.8 | 4.1 | 3.7 | 0.59 | **3.1** | **40%** |
| 2028 (Yr 2) | 19.8 | 10.2 | 9.6 | 0.78 | **8.8** | **44%** |
| 2029 (Phase 3) | 45.5 | 22.8 | 22.7 | 1.1 | **21.6** | **47%** |
| 2031 (Full) | 108 | 52.0 | 56.0 | 1.8 | **54.2** | **50%** |

> EBITDA excludes Pioneer Status CIT benefit. With Pioneer Status (5-year CIT holiday),
> free cash flow in years 2027–2031 improves by a further ~₦6.3 billion cumulatively.

### 4.2 Payback Analysis

| Investment | Amount | Annual Cash Flow | Simple Payback |
|---|---|---|---|
| Total Phase 1 CapEx | ₦5.1B | ₦3.1B (Year 1 EBITDA) | **1.6 years** |
| Energy system (solar + BESS) | ₦0.93B | ₦0.158B annual saving | **5.9 years** |
| Total Phase 1 + 2 CapEx | ₦6.9B | ₦8.8B (Year 2 EBITDA) | **< 1 year** (from Phase 2 completion) |

> The inverter factory's payback is extremely fast by manufacturing standards because:
> 1. Nigeria's 2M+/year inverter market demand is essentially guaranteed by chronic grid failure.
> 2. The Coo-Cah brand + SON certification commands a 27–40% premium vs. grey imports.
> 3. Gross margins in certified power electronics are 45–55% at B2B prices.
> 4. Pioneer Status eliminates CIT for 5 years — massively accelerating free cash flow.

### 4.3 Break-Even Analysis

| Metric | Value |
|---|---|
| Annual fixed cost base (Phase 1) | ~₦586M |
| Weighted average contribution margin | ~52% (blended product mix) |
| Break-even revenue | ₦586M / 0.52 = **₦1.13B** |
| Break-even at Phase 1 production | ~**14,500 inverter-equivalent units** |
| Phase 1 monthly target output | ~16,700 inverter-equivalent units |
| **Conclusion:** | Factory breaks even at **87% of Phase 1 target** |

---

## 5. Key Financial Risks

| Risk | Impact | Mitigation |
|---|---|---|
| Naira devaluation | Semiconductor costs rise in ₦ terms | USD-denominated FX hedging; local sourcing programme |
| Semiconductor shortage | Production halt if stock runs out | 90-day safety stock; dual-source policy |
| Electricity tariff increase | Energy cost increase | Solar + BESS already mitigates; ISO 50001 energy efficiency |
| Coo-Cah Plastics delay | Interim Lagos sourcing at 20% cost premium | 7-day safety stock buys time; interim suppliers identified |
| SON certification delay | Cannot sell commercially | Pre-compliance testing starts early; experienced SON consultant engaged |
| Project cost overrun | CapEx increases | 10% contingency built in; phased procurement |
| Competition (Chinese OEMs) | Price pressure | Quality differentiation; local warranty; SON certification as barrier |
