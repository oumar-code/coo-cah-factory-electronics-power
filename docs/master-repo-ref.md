# Master Repository Reference

This document establishes the formal traceability link between this factory repository and the
**Coo-Cah Technologies Holdings** master orchestrating repository.

---

## Master Repository

| Attribute | Value |
|---|---|
| **Repository** | [oumar-code/Coo-Kah-Doks](https://github.com/oumar-code/Coo-Kah-Doks) |
| **Purpose** | Single source of truth for strategy, architecture, blueprints, and group-wide standards |
| **Template Version Used** | v1.0 |
| **Factory Template Path** | `factories/_template/` |
| **Factory Blueprint Path** | `factories/electronics/garage-power-electronics/` |
| **Group Standards Path** | `docs/` (within master repo) |

---

## Factory Registration

| Attribute | Value |
|---|---|
| **Factory Name** | Coo-Cah Garage & Power Electronics Factory |
| **Factory Repository** | `coo-cah-factory-electronics-power` |
| **Registration Reference** | `orchestration/factory-status-registry.md` (in Coo-Kah-Doks) |
| **Vertical** | Electronics |
| **Sub-vertical** | Power Electronics |
| **Tier** | Tier 1 — Critical Infrastructure |
| **Phase** | Phase 1 (Planning) |
| **Status** | PLANNED |
| **Registered** | 2025 |

---

## Group-Wide Standards Applied

This repository follows all group-wide standards as defined in `docs/` within the master repo
[oumar-code/Coo-Kah-Doks](https://github.com/oumar-code/Coo-Kah-Doks). The following standards
are explicitly adopted and applied in this factory repository:

| Standard Area | Master Repo Reference | Applied In This Repo |
|---|---|---|
| ISO 9001:2015 — Quality Management | `docs/standards/iso-9001.md` | [docs/regulatory.md](./regulatory.md) |
| ISO 45001:2018 — Health & Safety | `docs/standards/iso-45001.md` | [docs/regulatory.md](./regulatory.md) |
| ISO 14001:2015 — Environmental (Phase 2) | `docs/standards/iso-14001.md` | [docs/regulatory.md](./regulatory.md) |
| ISO 50001:2018 — Energy (Phase 2) | `docs/standards/iso-50001.md` | [docs/energy-profile.md](./energy-profile.md) |
| Automation Phases Framework | `docs/automation/phases.md` | [docs/automation-roadmap.md](./automation-roadmap.md) |
| Supply Chain Doctrine | `docs/supply-chain/doctrine.md` | [docs/supply-chain.md](./supply-chain.md) |
| Energy Strategy | `docs/energy/strategy.md` | [docs/energy-profile.md](./energy-profile.md) |
| MES Integration Standards | `docs/mes/integration-standards.md` | [docs/mes-integration.md](./mes-integration.md) |
| AI Platform Standards | `docs/ai/platform.md` | [docs/digital-twin.md](./digital-twin.md) |
| Digital Twin Architecture | `docs/digital-twin/architecture.md` | [docs/digital-twin.md](./digital-twin.md) |
| Factory Blueprint Template | `factories/_template/` | All `docs/` files |
| Electronics Factory Blueprint | `factories/electronics/garage-power-electronics/` | All `docs/` files |

---

## Compliance Confirmation

This repository confirms adherence to the following group-wide requirements from the master repo:

- ✅ **Document format**: All documents use the standard markdown + Mermaid diagram format as
  defined in `factories/_template/` within Coo-Kah-Doks.
- ✅ **Naming conventions**: File names, SKU codes, zone labels, and machine designations follow
  the group-wide naming standards.
- ✅ **MES integration**: This factory adopts the group MES integration standard; all production
  data, serial numbers, and test records flow to the group MES platform as specified in
  `docs/mes/integration-standards.md`.
- ✅ **Automation phases**: Phase 1, 2, and 3 definitions in this repo are consistent with the
  group-wide automation phases framework.
- ✅ **Energy strategy**: The 600 kWp + 700 kWh BESS design follows the group energy
  independence strategy. Solar self-sufficiency target (≥ 80%) is the group standard.
- ✅ **Supply chain doctrine**: 90-day safety stock for air-freight semiconductors, dual-source
  policy, and intra-group supplier priority are all per the group supply chain doctrine.
- ✅ **Regulatory framework**: SON NIS, NCC Type Approval, NESREA, and NIPC Pioneer Status
  obligations are per the group Nigerian regulatory compliance framework.

---

## Version History

| Version | Date | Description | Author |
|---|---|---|---|
| 1.0 | 2025 | Initial factory repository creation — Phase 1 Planning | Coo-Cah Engineering Team |

---

## Related Repositories

| Repository | Relationship |
|---|---|
| [oumar-code/Coo-Kah-Doks](https://github.com/oumar-code/Coo-Kah-Doks) | Master orchestrating repo — strategy, blueprints, group standards |
| `coo-cah-factory-plastics-polymers` | Tier A intra-group supplier — plastic enclosures for this factory |
| `coo-cah-factory-personal-electronics` | Sister factory — RF pre-compliance lab for NCC Type Approval |
| `coo-cah-factory-bess-assembly` | Sister factory — potential Phase 2 LiFePO₄ pack supplier (UPS batteries) |
| `coo-cah-factory-metallurgical` | Sister factory — Phase 2 investigation for local transformer core sourcing |
