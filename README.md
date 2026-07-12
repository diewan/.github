<div align="center">

# DieWan

**Portable sanads. Local proof. No bridge authority.**

Client-side validation infrastructure for digital sanads that move across chains without moving trust into a bridge committee.

</div>

---

## The premise

Most cross-chain systems move an asset by introducing a new authority: a custodian, federation, relayer set, bridge contract, or wrapped representation.

DieWan takes a different route.

A sanad remains in client state. A chain-native seal enforces single use. When the seal is consumed, the sender produces evidence. The receiver accepts the sanad only after verifying that evidence.

**Proof travels. Custody does not.**

## What DieWan builds

| Layer | Function |
|---|---|
| **sanads** | Portable client-held state with explicit ownership and transfer rules |
| **Seals** | Chain-native single-use commitments anchored to each network's own guarantees |
| **Proofs** | Inclusion, finality, and state-transition evidence that can be independently checked |
| **Validation** | Local or destination-side verification before a sanad is accepted |
| **Developer systems** | SDKs, tooling, wallets, explorers, and agent interfaces around the protocol |

## Design principles

- **Native guarantees over simulated universality.** Each chain should enforce single use in the strongest form it natively supports.
- **Verification over attestation.** A receiver should inspect evidence rather than inherit somebody else's confidence.
- **Client state over global state.** Application state does not need to become universal consensus merely to become portable.
- **Explicit invariants over bridge folklore.** Security claims must be expressed as verifiable protocol conditions.
- **Minimal authority surfaces.** Every trusted operator added to a protocol becomes another institution users must eventually queue behind.

## The transfer model

1. A sanad is bound to a chain-specific seal.
2. The source-chain seal is consumed.
3. The sender constructs a proof bundle from chain data.
4. The receiver verifies inclusion, finality, and transition validity.
5. The sanad is accepted because the proof passes, not because an intermediary approved it.

## What DieWan is not

DieWan is not a custodial bridge, a wrapped-asset factory, a federation with nicer branding, or a promise that all chains are secretly the same machine.

It is a verification model for portable sanads across different machines.

## Current status

DieWan is under active private development.

The public [`csv-adapter`](https://github.com/diewan/csv-adapter) repository is an archived record of the original implementation direction. It remains available for historical and technical context, but it is not the current release surface.

Public specifications, SDKs, reference implementations, and integration material will appear here when they are ready to be depended upon.

## Public repository

| Repository | Purpose | Status |
|---|---|---|
| [`csv-adapter`](https://github.com/diewan/csv-adapter) | Original client-side validation and universal-seal implementation | Archived |

---

<div align="center">

**Verify before accepting.**

</div>
