# Trust Story: The Wandering Guest

An identity operating at the `guest` trust tier. This individual checked in 45 minutes ago. Their device fingerprint has changed, presence heartbeat is missing, and one risk event has occurred.

## Trust Condition Object

```json
{
  "identity_id": "abc123",
  "trust_tier": "guest",
  "time_since_last_proof": "45m",
  "geoip_expected_zone": true,
  "device_fingerprint_match": false,
  "risk_event_count": 1,
  "presence_heartbeat_missing": true,
  "decay_modifier": 1.2,
  "presence_score": 88,
  "trust_score": 72,
  "state": "Eroding"
}
```
