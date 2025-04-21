# Reservation Protocol

**A Presence-Based, Zero-Knowledge Trust Model for Modern Identity Security**

---

## Overview

**Reservation** is a rethinking of authentication and access—not as static logins, but as dynamic, presence-aware check-ins.

Instead of usernames, passwords, or even one-time MFA codes, Reservation relies on:
- Zero-Knowledge Proofs (ZKPs)
- Presence signals
- A decaying trust score computed in real time

Designed for both human and machine identities, Reservation introduces the concept of a **Trust Scoring Engine (TSE)** that erodes or reinforces trust based on context and time.

> "Every identity needs a reservation. Not just to get in—but to stay."

---

## Reservation Handshake Flow

1. **Arrival**: Device or identity emits a Presence Signal + ZKP
2. **Lobby Receives Proof**: Confirms it hasn’t been replayed, checks Reservation Token
3. **TSE Evaluates Trust Score** from a Trust Condition Object (TCO)
4. **Trust Status Rendered**: access granted, frictionless reproof, limited session, or denied
5. **Session Begins or Adjusts** based on live trust posture
6. **Trust Trail Logged** for future audit or correlation

### Trust Score Outcomes
| Trust Score | Trust Status | Outcome |
|-------------|--------------|---------|
| 80–100 | `approved` | Full access granted |
| 60–79 | `warning` | Silent reproof triggered |
| 40–59 | `decayed` | Limited access or alert triggered |
| <40 | `denied` | Session halted, re-verification required |

---

## Trust Scoring Engine (TSE)
The TSE uses both:
- **TCO presence signals** (time since proof, geo-IP match, risk event count)
- **Optional OSSTMM trust properties** (consistency, sufficiency, proximity, low vulnerability)

Example function output:
```json
{
  "trust_score": 64,
  "trust_status": "warning",
  "trust_notes": [
    "Consistent behavior observed.",
    "Signals deemed sufficient."
  ]
}
```

---

## Trust Condition Object (TCO) Example
```json
{
  "identity_id": "abc123",
  "trust_tier": "vendor",
  "time_since_last_proof": "45m",
  "geoip_expected_zone": true,
  "device_fingerprint_match": true,
  "risk_event_count": 0,
  "presence_heartbeat_missing": false,
  "decay_modifier": 1.1,
  "presence_score": 82,
  "trust_score": null,
  "state": "Eroding"
}
```

---

## Trust Tier Model (v1.0)
- `guest`  — short-lived sessions, fast decay
- `vendor` — moderate presence expectations
- `internal` — standard organizational users
- `executive` — VIP access, high monitoring
- `ai_agent` — machine identity, trust via behavior
- `service_account` — infrastructure identity, monitored for anomalies

---

## Future Roadmap
- **Airlock Zones** for pre-denial evaluation
- **TCO Anchoring** via blockchain or tamper-proof chains
- **Biometric ZKPs** (FaceID, TouchID, typing cadence)
- **Visual Trust Decay Timelines**
- **Reservation Token Issuance Protocol**

---

## Origin
Created by [GlassVault](https://theglassvault.net), Reservation is an ongoing R&D protocol at the intersection of trust, presence, privacy, and time.

---

## License
MIT

## Contributors
John Daniel – Identity architect, researcher, and founder of GlassVault



