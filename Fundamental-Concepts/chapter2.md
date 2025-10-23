# Chapter 2 – The Basics of Cybersecurity 

## 1. The CIA Triad: Confidentiality, Integrity, Availability

Think of the CIA triad as the three pillars that hold up every security program.

### Confidentiality – “Who gets to see it?”

Only the right people should ever peek at your data.

- **How we protect it:** passwords, multi‑factor authentication (MFA), encryption, and clear data‑handling rules.  
- **What goes wrong if it’s broken:** eavesdropping, data breaches, insider leaks—anyone who isn’t supposed to see the information ends up with it.

### Integrity – “Has it been tampered with?”

Your data must stay exactly the way it was meant to be, unless an authorized change is made.

- **How to achieve this:** hashing (think SHA‑256), digital signatures, checksums, version‑control systems, regular backups.  
- **Consequences:** malware that silently rewrites files, man‑in‑the‑middle attacks that alter traffic, corrupted databases.

### Availability – “Can I get it when I need it?”

Even the most secret, perfectly intact data is useless if you can’t reach it.

- **Protective measures:** redundancy (RAID, server clusters), frequent backups, disaster‑recovery plans, DDoS mitigation, timely patching.  
- **Problems that may occur:** DDoS floods, hardware failures, ransomware that locks you out, power cuts.


## 2. Non‑Repudiation – “No One Can Walk Away Saying ‘I Didn’t Do That’”

Non‑repudiation makes sure a user can’t later deny having performed an action. It’s crucial for legal, financial, and audit situations.

- **How we achieve it:** digital signatures backed by public‑key infrastructure (PKI), immutable audit logs with timestamps, message authentication codes (MACs). 
- **Real‑world example:** You sign a PDF contract with a digital certificate. The signature proves who signed it *and* guarantees the document hasn’t been altered since.


## 3. AAA – Authentication, Authorization, Accounting

AAA is the security “check‑list” that tells us who you are, what you’re allowed to do, and what you actually did.

| Step | What it means | Typical tools |
|------|---------------|----------------|
| **Authentication** | Prove your identity. | Passwords, biometrics, smart cards, MFA. |
| **Authorization** | Decide what resources you can touch. | Role‑Based Access Control (RBAC), ACLs, principle of least privilege. |
| **Accounting (Auditing)** | Record what you’ve done. | System logs, session records, audit trails. |

A handy mnemonic: **AAA = “Who are you? What can you do? What did you do?”**

## 4. Zero‑Trust Architecture (ZTA) – “Never Trust, Always Verify”

Zero trust flips the old idea of a “trusted interior” on its head. Whether a user is inside the corporate LAN or connecting from a coffee shop, you treat them as untrusted until proven otherwise.

### Key ideas
- **Verify explicitly** – Continuously check identity, device health, location, and behavior.  
- **Least‑privilege access** – Give people only the permissions they truly need.  
- **Assume breach** – Design systems assuming attackers may already be inside.  
- **Micro‑segmentation** – Break the network into tiny zones so an intruder can’t roam freely.  
- **Continuous monitoring** – Spot anomalies fast and react.

### Enablers you’ll see in practice
- Multi‑factor authentication (MFA)  
- Robust identity‑and‑access‑management (IAM) platforms  
- Endpoint detection and response (EDR) tools  
- Security information and event management (SIEM) solutions  
- Network encryption and tight segmentation  

### Why it matters
It slashes the attack surface, curbs insider threats, and gives you far better visibility into who’s doing what.

## 5. Deception & Disruption Technologies – “Turn the Tables on Attackers”

Instead of waiting passively for an intrusion, these techniques actively *bait* and *break* attackers.

### Deception Technology – “Set the trap”
- **What it is:** Fake assets (servers, databases, credentials) that look real but are actually honeypots or honeytokens.  
- **Typical flavors:**  
  - **Honeypots** – Stand‑alone fake servers that lure attackers.  
  - **Honeytokens** – Dummy credentials or files that trigger alerts the moment someone tries to use them.  
  - **Honeynets** – Whole networks of decoys mimicking a real environment.  
- **Why use them:** Early breach detection, insight into attacker tactics, and wasting the adversary’s time.

### Disruption Technology – “Knock them down”
- **What it is:** Automated actions that isolate or cripple malicious activity as soon as it’s spotted.  
- **Common tactics:**  
  - Quarantining compromised endpoints.  
  - Cutting off command‑and‑control (C2) channels.  
  - Deploying fake C2 responses or corrupting stolen data.  
- **Goal:** Contain the threat, confuse the attacker, and buy defenders precious time to remediate.

Together, deception and disruption give you a proactive edge—detecting threats early, gathering intel, and shortening the window attackers have to cause damage.
