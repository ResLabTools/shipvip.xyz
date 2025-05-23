# SHIPVIP DevNet – Internal Testing Environment

This repository contains internal documentation and endpoint structure for the SHIPVIP Logistics Management Platform (DevNet 2025).

> For use with SHIPVIP sandbox services only. Not connected to production APIs.

---

## Endpoints

- `POST /api/auth/reset`
- `GET /api/track?tracking_id=...`
- `POST /api/shipment/create`
- `GET /api/zone-matrix`
- `POST /webhooks`

> Refer to [SHIPVIP_Rates_2025.pdf](docs/SHIPVIP_Rates_2025.pdf) and [SHIPVIP_Zones_2025.pdf](docs/SHIPVIP_Zones_2025.pdf)

---

## Auth Structure

All requests require a valid `access_key`. Expiry is 48 hours. DevNet keys are rotated manually via admin panel.

---

## Sandbox Mode Flags

- `simulate_delay=true`
- `scan_failure=true`
- `sandbox=true`

---

**DevNet ID:** SHIPVIP-STAGING-ENV-2025  
**Contact:** https://shipvip.xyz/admin/help


