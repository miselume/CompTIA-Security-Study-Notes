# 💤 Lazy Notes – Cybersecurity Essentials  

## The CIA Triad – Core Pillars of Information Security  

| Pillar            | What It Means                                   | Typical Controls                                                                 |
|-------------------|-------------------------------------------------|-----------------------------------------------------------------------------------|
| **Confidentiality** | Only authorized parties can read the data.       | • Strong passwords<br>• Multi‑factor authentication (MFA)<br>• End‑to‑end encryption<br>• Role‑based access controls |
| **Integrity**        | Data remains unchanged unless properly modified. | • Cryptographic hashes<br>• Digital signatures<br>• Version control systems<br>• Integrity‑checking tools |
| **Availability**     | Information and services are accessible when needed. | • Regular backups<br>• Disaster‑recovery plans<br>• DDoS mitigation<br>• Timely patching<br>• Redundant infrastructure |

### Common Threats per Pillar  

- **Confidentiality** – eavesdropping, data breaches, insider leaks.  
- **Integrity** – malware tampering, man‑in‑the‑middle attacks, corrupted databases.  
- **Availability** – DDoS attacks, hardware failures, ransomware, power outages.

---

## Non‑Repudiation

Ensures a party cannot deny having performed an action.

**How it’s achieved**
- **Digital signatures** using a PKI (public‑key infrastructure)  
- **Immutable audit logs** with trusted timestamps  

These mechanisms provide verifiable proof of who did what and when.

---

## AAA – Authentication, Authorization, Accounting

*Authentication*: Verifies who you are (e.g., login credentials).

*Authorization*: Determines what resources you may access once authenticated.

*Accounting*: Records what you did (system logs), providing an audit trail.

Tip: Accounting logs actions; non‑repudiation adds cryptographic protection so those logs can’t be denied or tampered with.

---

## Zero‑Trust Architecture (ZTA)

1. Assume every request is untrusted and continuously verify identity (MFA, strong IAM).
2. Enforce least‑privilege access for users, devices, and services.
3. Segment networks into isolated zones so a breach can’t move laterally.
4. Monitor constantly with EDR and SIEM to detect anomalous behavior.
5. Encrypt all traffic across the network and between components.

In short: always verify, limit permissions, isolate resources, and keep watch.

---

## Deception & Disruption Technologies

Deception – set traps to expose and waste attackers’ time.

- Honeypots: Isolated fake servers.

- Honeytokens: Dummy credentials or data that trigger alerts when used.

- Honey‑net: A network of decoy systems mimicking a real environment.

Disruption – automatically neutralize malicious activity once detected.

- Quarantine: Isolate compromised endpoints.
- C2 Cut‑off: Block command‑and‑control communications.

Together, deception gathers intel and delays attackers, while disruption stops them in their tracks.
