# BIM Evidence Pack Overview

**Factory:** Coo-Cah Garage & Power Electronics Factory, Sagamu, Ogun State  
**Repository:** `coo-cah-factory-electronics-power`  
**Document Ref:** CCG-PE-BIM-000 | **Version:** 1.0  
**Dataset Status:** Design baseline package assembled; production sign-off pending

---

## 1. Purpose

This document is the entry point for the BIM evidence pack used by the Digital Twin and MES
spatial loaders. It defines the scope, coordinate basis, load order, and sign-off path for the
factory-specific BIM artifacts in this repository.

---

## 2. Scope

The BIM evidence pack for this factory includes only the factory-specific deltas required by the
group DT standards:

- spatial zone definitions in `zone-boundaries.md`
- fixed-asset anchor definitions in `asset-anchors.md`
- references back to `../floor-plan.md`, `../machinery.md`, and `../digital-twin.md`

This package does not override any group DT schema, naming, or platform rule defined in
**Coo-Kah-Doks**.

---

## 3. Coordinate Reference System

**Authoritative CRS:** `CCG-PE-SAG-LCS-01`

- Origin: south-west corner of the site perimeter
- X axis: east
- Y axis: north
- Z axis: metres above finished floor / finished pad level

All polygons and fixed-asset anchors in this BIM package must use this site-local CRS.

---

## 4. Load Order Rule

The BIM evidence pack must be loaded in the following order:

1. `zone-boundaries.md` — establish the approved spatial envelope and zone identifiers
2. `asset-anchors.md` — load fixed-asset anchors only after zone IDs are resolved successfully
3. `../sensor-map.md` — validate that active telemetry points reference approved assets and zones

**Control rule:** no partial publication is allowed for production release. If the zone dataset is
not frozen, the anchor dataset cannot be promoted.

---

## 5. Evidence Package Contents

| Artifact | Purpose | Current Role |
|---|---|---|
| [Zone Boundaries](./zone-boundaries.md) | Spatial polygons and zone controls | Pass 7A evidence |
| [Asset Anchors](./asset-anchors.md) | Fixed-asset coordinates and orientation | Pass 7B evidence |
| [Sensor Registry](../sensor-map.md) | Asset/zone-linked telemetry baseline | Pass 8 dependency |
| [Full Readiness Register](../readiness-register.md) | Canonical gate tracker | Governance source of truth |

---

## 6. Sign-Off Path

| Step | Required Owner | Evidence |
|---|---|---|
| Zone geometry review | Digital Twin Lead | IFC import package + geometry QA |
| Physical correspondence review | Facilities Lead | Site walkdown confirmation |
| Asset-position review | Controls Engineering Lead | Install walkdown pack |
| Production publication approval | MES Lead + Digital Twin Lead | Signed publication package |

---

## 7. Current Publication Posture

This BIM package is prepared for the two-week DT readiness sprint, but it is **not yet production
published**. External sign-offs, final IFC import evidence, and walkdown completion remain governed
in the linked evidence documents.

---

## 8. Related Documents

- [Zone Boundaries](./zone-boundaries.md)
- [Asset Anchors](./asset-anchors.md)
- [Sensor Registry](../sensor-map.md)
- [Full Readiness Register](../readiness-register.md)
