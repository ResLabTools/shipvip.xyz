# SHIPVIP API Integration Guide (DevNet)

This guide walks you through the basic integration steps with SHIPVIP's DevNet test environment.

## Step 1: Get API Credentials

Use `POST /api/auth/reset` to rotate your token. You will receive:
- `access_key`
- `expires_at`
- `scopes`

## Step 2: Create Shipment

Use `POST /shipment/create` with:
```json
{
  "recipient": "John Smith",
  "zone": "4",
  "weight": 2.4,
  "priority": "overnight"
}
```

## Step 3: Track Shipment

```bash
GET /api/track?tracking_id=SVP-404-XYT93
```

Returns:
```json
{
  "status": "Delivered",
  "timestamp": "2025-05-22T10:32:01Z",
  "zone": "4"
}
```

## Errors

- `403`: Token expired or missing sandbox flag
- `502`: DevNet outage (try again in 2–5 minutes)

More help: https://shipvip.xyz/admin/help
