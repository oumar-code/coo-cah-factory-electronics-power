# Coo-Cah Garage & Power Electronics Factory

![Status: PLANNED](https://img.shields.io/badge/Status-PLANNED-yellow)
![Tier: 1 — Critical Infrastructure](https://img.shields.io/badge/Tier-1%20Critical%20Infrastructure-red)
![Phase: 1](https://img.shields.io/badge/Phase-1-blue)
![Location: Sagamu, Ogun State](https://img.shields.io/badge/Location-Sagamu%2C%20Ogun%20State-green)
![Master Repo: Coo-Kah-Doks](https://img.shields.io/badge/Master%20Repo-Coo--Kah--Doks-purple)

> **Tier 1 Critical Infrastructure** — This factory manufactures the energy resilience products that every
> other Coo-Cah factory depends on. It is a Phase 1 priority, commissioned at the same time as or before
> revenue-generating Tier 2 factories. See [MASTER_REPO_REF.md](./MASTER_REPO_REF.md) for traceability
> back to the [Coo-Kah-Doks](https://github.com/oumar-code/Coo-Kah-Doks) master repository.

---

## Factory Overview

| Attribute | Value |
|---|---|
| **Factory Name** | Coo-Cah Garage & Power Electronics Factory |
| **Repository** | `coo-cah-factory-electronics-power` |
| **Vertical** | Electronics |
| **Sub-vertical** | Power Electronics — Inverters, Solar Charge Controllers, UPS, Battery Chargers, Power Tools |
| **Location** | Sagamu Industrial Estate, Ogun State, Nigeria |
| **Tier** | Tier 1 — Critical Infrastructure |
| **Phase** | Phase 1 (Planning / Development) |
| **Status** | PLANNED |
| **Facility Area** | ~12,000 m² |
| **Direct Employees** | ~280 (Phase 1) |
| **Indirect Employees** | ~60 (Phase 1) |
| **Estimated Peak Load** | ~400 kW |
| **Solar PV** | 600 kWp — ground-mount |
| **BESS** | 700 kWh LFP (CATL/BYD containerised) |
| **Backup Generator** | 1 × Perkins 400 kVA diesel, 1,500 L tank (~60 h at 40% load) |
| **Quality Standards** | ISO 9001:2015 (Phase 1); ISO 14001 + ISO 50001 (Phase 2) |
| **Safety Standard** | ISO 45001:2018 |
| **Regulatory** | SON NIS, NCC Type Approval, NESREA, NIPC Pioneer Status |

---

## Products — Phase 1 SKUs

| SKU Code | Product | Variants | Phase |
|---|---|---|---|
| **CCG-INV-PSW** | Pure Sine Wave Inverter | 300VA / 500VA / 1kVA / 2kVA / 3kVA / 5kVA | Phase 1 |
| **CCG-INV-MSW** | Modified Sine Wave Inverter | 300VA / 500VA / 1kVA / 2kVA | Phase 1 |
| **CCG-SCC-MPPT** | MPPT Solar Charge Controller | 20A / 40A / 60A / 100A | Phase 1 |
| **CCG-SCC-PWM** | PWM Solar Charge Controller | 10A / 20A / 30A | Phase 1 |
| **CCG-SPK** | Solar Panel Kit (packaged) | 100W / 200W / 400W | Phase 1 |
| **CCG-BC** | Smart Multi-Stage Battery Charger | 12V / 24V / 48V systems | Phase 1 |
| **CCG-PS** | Surge-Protected Smart Power Strip (Wi-Fi) | 4-way / 6-way / 8-way | Phase 1 |
| **CCG-UPS** | Line Interactive UPS | 600VA / 1kVA / 2kVA | Phase 1 |
| **CCG-PT-DRILL** | Electric Drill | Corded 500W/750W; Cordless 18V | Phase 1 |
| **CCG-PT-AG** | Angle Grinder | 115mm / 125mm (700W–1000W) | Phase 1 |
| **CCG-PT-CS** | Circular Saw | 165mm / 185mm (1200W–1600W) | Phase 1 |

### Phase 1 Starting Focus (Early Revenue + Internal Demand)

| SKU | Variant | Rationale |
|---|---|---|
| CCG-INV-PSW | 2kVA + 3kVA | Highest internal and external demand immediately |
| CCG-SCC-MPPT | 40A + 60A | Required by Coo-Cah energy systems team for all solar installations |
| CCG-PS | 4-way / 6-way | High volume, simple to manufacture, fast ramp-up |

---

## Production Capacity Targets

| Product Line | Phase 1 (2025–2026) | Phase 2 (2027–2028) | Phase 3 (2029–2031) |
|---|---|---|---|
| Inverters (all sizes) | 200,000 units/year | ~450,000 units/year | 700,000 units/year |
| Solar Charge Controllers | 150,000 units/year | ~320,000 units/year | 500,000 units/year |
| Battery Chargers | 80,000 units/year | ~160,000 units/year | 250,000 units/year |
| Power Strips | 500,000 units/year | ~1,000,000 units/year | 1,500,000 units/year |
| UPS | 50,000 units/year | ~130,000 units/year | 250,000 units/year |
| Power Tools | 100,000 units/year | ~280,000 units/year | 500,000 units/year |

---

## Strategic Role — Why Tier 1 Critical

This factory is classified **Tier 1 Critical Infrastructure** because it manufactures the power
resilience products that **every other Coo-Cah factory depends on** to operate.

### Internal Dependency Chain

Every Coo-Cah factory site requires:

| Product | Use Case at Sister Factories |
|---|---|
| PSW Inverter (3kVA / 5kVA) | Backup power when grid and BESS are depleted |
| UPS (1kVA rack-mount) | Protection for MES server rooms and IT infrastructure |
| MPPT Solar Charge Controller | All rooftop and ground-mount solar installations |
| Smart Power Strip (CCG-PS) | All workstations and production equipment |
| Power Tools (Drill + Grinder) | All factory maintenance workshops |

Without this factory operational, the entire Coo-Cah energy independence strategy depends on
imported products — with foreign-currency cost exposure, long lead times, and no local warranty
support. This factory eliminates that dependency.

### Nigerian Market Opportunity

Nigeria's inverter and solar market exceeds **2 million units per year**, growing at 15–20% annually
driven by chronic grid instability (8–12 h DISCO supply per day in most states). The Coo-Cah brand
positioning — **Premium Performance + Mid-Market Price + Local Warranty** — combined with a
factory-direct aftersales centre in Sagamu creates a durable competitive moat.

---

## Dependency Map

### This Factory Supplies (Outbound — Internal Priority First)

```
┌─────────────────────────────────────────────────────────────┐
│           Coo-Cah Garage & Power Electronics Factory        │
│                    (Sagamu, Ogun State)                     │
└──────────────────────┬──────────────────────────────────────┘
                       │  OUTBOUND SUPPLY
        ┌──────────────┼──────────────┐
        ▼              ▼              ▼
  All Coo-Cah    MES Server Rooms   Solar Install
  Factories      at All Sites        Team
  (Inverters,    (UPS 1kVA)         (MPPT SCCs)
  Power Strips,
  Power Tools)
```

| Destination | Product | Notes |
|---|---|---|
| All Coo-Cah factories | PSW Inverter (3kVA / 5kVA) | Internal priority before commercial sales |
| All Coo-Cah factories | UPS (1kVA rack-mount) | MES server room protection |
| Coo-Cah energy team | MPPT Solar Charge Controllers | All solar installations across the network |
| All Coo-Cah factories | Smart Power Strips (CCG-PS) | IT and production workstations |
| All Coo-Cah factories | Power Tools (Drill + Grinder) | Maintenance workshops |
| External B2B + Retail | All commercial SKUs | Begins when Phase 1 ramp exceeds internal demand |

### This Factory Receives (Inbound)

| Source | Material / Component | Lead Time | Safety Stock |
|---|---|---|---|
| **Coo-Cah Plastics & Polymers Factory** (Agbara) | Plastic enclosures, housings, power strip bodies | 1–2 days (intra-group, 60 km by road) | 7 days |
| Infineon Technologies (Germany) | Power MOSFETs / IGBTs | Air freight; ~5–7 days + customs | 90 days |
| Texas Instruments (USA) | Gate Driver ICs | Air freight; ~5–7 days + customs | 90 days |
| Baoding Tianwei / China | Toroidal / EI transformer cores | Sea freight; 22–28 days | 60 days |
| Kabelmetal Nigeria / India | Magnet wire (copper winding wire) | Local 3–7 days / Import 14–21 days | 21 days |
| Nichicon / Rubycon (Japan) | Electrolytic capacitors | Air freight (critical); sea (standard) | 45 days |
| China / Taiwan OEM | PCB bare boards | LCL sea freight; 4–6 weeks | 30 days |
| CSB Battery / Vision (HK/Taiwan) | UPS VRLA batteries | Sea freight (DG — IMDG class) | 30 days |
| Longi / JA Solar / Canadian Solar | Solar panels (for CCG-SPK kits) | Sea freight | 45 days |

---

## Energy Profile Summary

| Parameter | Value |
|---|---|
| Facility Area | ~12,000 m² |
| Estimated Peak Load | ~400 kW |
| Daily Energy Consumption | ~2,800 kWh/day |
| Solar PV | 600 kWp — ground-mount (east of building + car park shade) |
| BESS | 700 kWh LFP (CATL/BYD containerised) |
| Solar Irradiance | 4.7 PSH/day average; 4.5 PSH/day worst month |
| Target Solar Self-Sufficiency | ≥ 80% |
| Grid Supply (Sagamu DISCO) | ~8–12 h/day |
| Backup Generator | 1 × Perkins 400 kVA diesel; 1,500 L tank (~60 h at 40% load) |

> Ogun State (Sagamu) grid supply is limited to 8–12 h/day. The 600 kWp + 700 kWh system is
> designed to make the factory effectively grid-independent during all production hours.
> Ground-mount is preferred over rooftop: Sagamu has available land east of the building, avoids
> rooftop structural loading, and provides shaded car parking.

See [docs/energy-profile.md](./docs/energy-profile.md) for full demand analysis and cost model.

---

## Documentation Index

| Document | Description |
|---|---|
| [MASTER_REPO_REF.md](./MASTER_REPO_REF.md) | Master repo traceability, version reference, group standards |
| [docs/machinery.md](./docs/machinery.md) | Full equipment register: SMT line, winding machines, assembly, test, AMR |
| [docs/energy-profile.md](./docs/energy-profile.md) | Power demand analysis, solar design, BESS, energy cost model |
| [docs/floor-plan.md](./docs/floor-plan.md) | 12,000 m² layout: zones, flow paths, solar yard, BESS pad |
| [docs/automation-roadmap.md](./docs/automation-roadmap.md) | Phase 1 → 3 automation strategy: SMT, CNC winding, lights-out |
| [docs/supply-chain.md](./docs/supply-chain.md) | Semiconductor procurement, intra-group suppliers, market opportunity |
| [docs/regulatory.md](./docs/regulatory.md) | SON NIS, NCC Type Approval, NESREA, Pioneer Status |
| [docs/capex-opex.md](./docs/capex-opex.md) | Phased CapEx, unit economics, BOM cost model, payback analysis |
| [docs/digital-twin.md](./docs/digital-twin.md) | Asset registry, SMT + winding DT, energy monitoring |
| [docs/mes-integration.md](./docs/mes-integration.md) | Serial traceability, IEC 62040 records, load bank integration |

---

## Phase 1 Milestone Checklist

| # | Milestone | Target Date | Status |
|---|---|---|---|
| M1 | NIPC Pioneer Status application submitted | Q3 2025 | 🔲 Planned |
| M2 | NESREA EIA (Environmental Impact Assessment) submitted | Q3 2025 | 🔲 Planned |
| M3 | Factory site acquired / lease signed (Sagamu Industrial Estate) | Q4 2025 | 🔲 Planned |
| M4 | Civil construction commenced | Q1 2026 | 🔲 Planned |
| M5 | Ground-mount solar civil works commenced (600 kWp) | Q1 2026 | 🔲 Planned |
| M6 | SMT line installed and commissioned | Q2 2026 | 🔲 Planned |
| M7 | BESS (700 kWh LFP) energised | Q2 2026 | 🔲 Planned |
| M8 | Transformer winding cells operational | Q2 2026 | 🔲 Planned |
| M9 | MES deployed across all production zones | Q2 2026 | 🔲 Planned |
| M10 | AMR fleet (12 units) commissioned | Q3 2026 | 🔲 Planned |
| M11 | First CCG-INV-PSW 2kVA prototype tested | Q3 2026 | 🔲 Planned |
| M12 | First CCG-SCC-MPPT 40A prototype tested | Q3 2026 | 🔲 Planned |
| M13 | SON NIS type-test samples submitted | Q4 2026 | 🔲 Planned |
| M14 | NCC Type Approval submitted (CCG-PS Wi-Fi strips) | Q4 2026 | 🔲 Planned |
| M15 | ISO 9001:2015 certification audit | Q4 2026 | 🔲 Planned |
| M16 | First internal deliveries to sister factories | Q1 2027 | 🔲 Planned |
| M17 | Commercial sales launch (B2B + retail) | Q2 2027 | 🔲 Planned |

---

## Master Repository

This factory repository is part of the **Coo-Cah Technologies Holdings** manufacturing ecosystem.
The master orchestrating repository is [oumar-code/Coo-Kah-Doks](https://github.com/oumar-code/Coo-Kah-Doks).

All group-wide standards (ISO requirements, automation phases, supply chain doctrine, energy strategy,
AI platform, MES integration standards) are defined in the master repo and this repository is fully
traceable back to those standards. See [MASTER_REPO_REF.md](./MASTER_REPO_REF.md) for details.
