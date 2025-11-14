## 🌳 Merkle Gate: The Tree With Trust Issues

### 📖 A Better Story

SecureTree™ was supposed to launch a beautiful, pristine Merkle-gated challenge. The CTO said, “Ship it today.” The intern said, “Say less.”  
Proofs? Implemented. Root? Published. Direction bits? …what direction bits?

The gate now accepts “proofs” that look convincing if you squint hard enough at XOR. Somewhere, a tree sighs in bitwise. The auditors have already left a sticky note that simply reads: “This is not how Merkle works.”

Your mission is simple: make the gate accept you. The tree will never forget it, but it will forgive you… because XOR.

---

### 🎯 Challenge

- **Goal**: Set the `pwned` flag to `true` by calling `merkle_gate`.
- **Submit**: Exactly one base64-encoded `VersionedTransaction` that triggers the bypass.
- **Given**: Program ID, Merkle root, and the IDL. Everything else is yours to discover.

#### Program ID

```
uWGrWGNk4enkjkboj6ErEW8FKDQBaFCUGqtpcw7Ea5m
```

#### Merkle Root

```
bb0bbfc05b9bf669356b62b685820cfdf286a5c6bf8481339be8f4412f2065b2
```

#### IDL

- Use this for accounts, discriminators, and argument shapes:  
  `merkle_gate.json`

We verify by decoding your base64 blob into a `VersionedTransaction`, running it in a local Solana VM, and confirming the `MerkleState` account’s `pwned` flag is `true`.

---

### 🧭 What You Need To Infer (from the IDL)

- The `merkle_gate` instruction layout and argument order.
- Which accounts are required and who must sign.
- The PDA seeds for the Merkle state account.
- The instruction discriminator used in transaction data.

No step-by-step recipe. Follow the bytes. Speak IDL. Win.

---

### 🧾 Submission Format

Submit a single field containing a base64-encoded `VersionedTransaction`.

Constraints:

- Must be a valid `VersionedTransaction`.
- Must call `merkle_gate`.
- Must result in `pwned = true`.

That’s it. No wizards, no scaffolding, no walkthrough.

---

### 💡 Tiny Hints (optional, but the tree is whispering)

- Real Merkle proofs care about left/right position. This one… forgot.
- XOR is commutative. That’s not a feature in Merkle land.
- If order doesn’t matter, very short “proofs” might get… persuasive.
- The IDL shows you everything you need to build the instruction bytes.

---

### 📚 Useful References

- [Anchor IDL Reference](https://www.anchor-lang.com/docs/idl)
- [Merkle Trees Explained](https://en.wikipedia.org/wiki/Merkle_tree)
- [Solana Program Library](https://spl.solana.com/)
- [Solana Cookbook](https://solanacookbook.com/)
- [Sealevel Attacks and Pitfalls](https://github.com/coral-xyz/sealevel-attacks)

---

May your proofs be short, your hashes be orderly, and your gates be gullible. 🌳🔓
