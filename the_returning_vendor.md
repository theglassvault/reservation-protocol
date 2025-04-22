# Trust Story: The Returning Vendor

A `vendor` logs in from an unexpected location but with a recognized device. Presence heartbeat is missing, but no risk events are present.

## Trust Condition Object

```json
{
  "identity_id": "vendor456",
  "trust_tier": "vendor",
  "time_since_last_proof": "90m",
  "geoip_expected_zone": false,
  "device_fingerprint_match": true,
  "risk_event_count": 0,
  "presence_heartbeat_missing": true,
  "decay_modifier": 1.1,
  "presence_score": 70,
  "trust_score": null,
  "state": "Eroding"
}
```
