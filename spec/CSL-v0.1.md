# CSL v0.1 — Protocol Specification
HBCE Civic Signal Layer
Consultive · Opposable · Auditable

Status: Draft v0.1  
Mode: Experimental (Consultive Only)

---

## 1. Purpose

CSL defines a territorial, consultive voting signal system gated by IPR.

The system produces cryptographically verifiable voting signals
without replacing institutional electoral processes.

CSL is designed for:

- Governance modeling
- Civic signal experimentation
- Territorial participation analysis
- Cryptographic accountability testing

---

## 2. Core Principles

1. EU-first alignment
2. Audit-first architecture
3. Fail-closed verification
4. Append-only ledger
5. Hash-only public exposure
6. Pseudonymous public identity
7. External legal identity custody

---

## 3. System Actors

### 3.1 IPR Holder
- Must have activated IPR
- Holds cryptographic key pair
- Can vote within territorial eligibility

### 3.2 Verifier
- Validates ledger integrity
- Validates vote receipt
- Ensures hash-chain continuity

### 3.3 Observer
- Can read proposals
- Can verify votes
- Cannot modify ledger

---

## 4. Territorial Gating Model

Eligibility is derived from verified territorial attributes
stored outside public ledger and represented as hash commitments.

Territorial hierarchy:

- Neighborhood
- City
- Region
- State
- European Union

Vote scope must match territorial eligibility.

Fail condition:
If territorial verification fails → vote rejected (fail-closed).

---

## 5. Vote Object Structure

A vote must contain:

- proposal_id
- territory_level
- vote_choice (YES | NO | ABSTAIN)
- voter_public_key
- timestamp (ISO 8601)
- signature

Votes are immutable once submitted.

---

## 6. Receipt Model

Each valid vote produces:

- vote_hash
- ledger_entry_hash
- timestamp
- verifier_hash
- signature_validation_status

Receipt allows independent verification.

---

## 7. Ledger Structure

Ledger is append-only.

Each entry contains:

- entry_index
- previous_hash
- vote_hash
- timestamp
- entry_hash

Ledger continuity must be deterministic.

Any mismatch → system status = INVALID (fail-closed).

---

## 8. Legal Positioning

CSL v0.1:

- Is consultive
- Has no electoral authority
- Produces civic signal only
- Is research-grade infrastructure

Future legal integration requires:
- eIDAS compatibility review
- GDPR compliance audit
- Institutional partnership

---

## 9. Versioning

v0.1 — Specification Bootstrap  
Future versions require backward integrity compatibility.

End of Specification.
