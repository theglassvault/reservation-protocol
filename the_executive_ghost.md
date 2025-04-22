# Trust Story: The Executive Ghost

A high-privilege user hasn't checked in for over 5 hours. Session is still open on a personal device. Presence heartbeat missing, and two minor risk events have been logged.

## Trust Condition Object

```json
{
  "identity_id": "exec777",
  "trust_tier": "executive",
  "time_since_last_proof": "300m",
  "geoip_expected_zone": true,
  "device_fingerprint_match": true,
  "risk_event_count": 2,
  "presence_heartbeat_missing": true,
  "decay_modifier": 0.9,
  "presence_score": 30,
  "trust_score": null,
  "state": "At-Risk"
}
```
