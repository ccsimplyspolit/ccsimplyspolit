# Serhii Shunko (`@sshunko` / `@ccsimplyspolit`)

**Independent Systems & Binary Security Researcher**  
Focus: C/C++ Memory Safety, Binary Protocol Fuzzing (`libFuzzer` / `libprotobuf-mutator` / ASAN), Virtual Machine Deserialization Internals, and AI/MCP Infrastructure Security.

- **Security Research Portal & Advisory Index:** [https://ccsimplyspolit.github.io](https://ccsimplyspolit.github.io)
- **ORCID:** [0009-0002-4183-0361](https://orcid.org/0009-0002-4183-0361)
- **GitHub:** [@ccsimplyspolit](https://github.com/ccsimplyspolit)
- **HackerOne:** [https://hackerone.com/sshunko](https://hackerone.com/sshunko)
- **Contact & Coordinated Disclosure:** `cc.simply.spolit@gmail.com`

---

## 0x00 // Confirmed Vulnerability Disclosures (CVD)

> **[CVD Policy]** Only vendor-accepted advisories and bounty-awarded disclosures are listed below. Active reports still undergoing initial maintainer triage remain strictly private until upstream confirmation.

| Advisory ID | Target Component | CWE | Component Scope | Status |
| :--- | :--- | :--- | :--- | :--- |
| [`GHSA-cr23-59mg-h2rc`](https://ccsimplyspolit.github.io/advisories/GHSA-cr23-59mg-h2rc.html) | `bacnet-stack/bacnet-stack` ([GHSA](https://github.com/bacnet-stack/bacnet-stack/security/advisories/GHSA-cr23-59mg-h2rc)) | `CWE-125` / `CWE-787` / `CWE-400` / `CWE-835` | Out-of-Bounds Read, Unbounded Allocation & Infinite Loop in `src/bacnet/lighting.c` & `bactext.c` | **Accepted by Vendor (`draft` GHSA) • [Upstream Fix PR `#1595`](https://github.com/bacnet-stack/bacnet-stack/pull/1595)** |
| [`GHSA-qm7x-j9xp-x3gv`](https://ccsimplyspolit.github.io/advisories/GHSA-qm7x-j9xp-x3gv.html) | `czlonkowski/n8n-mcp` ([GHSA](https://github.com/czlonkowski/n8n-mcp/security/advisories/GHSA-qm7x-j9xp-x3gv)) | `CWE-918` / `CWE-184` | SSRF Protection Bypass in `validateUrlSync` & `validateWebhookUrl` via Trailing-Dot FQDNs & `*.localhost` | **Confirmed & Patched in `v2.99.2` ([commit `a49dfb4`](https://github.com/czlonkowski/n8n-mcp/commit/a49dfb4))** |
| [`H1-4148578`](https://ccsimplyspolit.github.io/advisories/H1-4148578.html) | `brave/ai-gateway` (Brave Software) | `CWE-20` / `CWE-755` | Unhandled Exception & Input Validation Flaw in Model Request Validation Pipeline | **Confirmed by Vendor (HackerOne `#4148578`) • Bounty Awarded ($50.00)** |

---

## 0x01 // Technical Methodology Write-ups

1. **[Anatomy of Unsigned Integer Underflows & Sticky-State Stack Overflows in C/C++ Parsers](https://ccsimplyspolit.github.io/writeups/integer-underflow-packet-parsers.html)** (`CWE-191` / `CWE-121`)
2. **[Structure-Aware Fuzzing of High-Frequency RPC & Simulation Protocols with libprotobuf-mutator](https://ccsimplyspolit.github.io/writeups/libprotobuf-mutator-subtick-invariants.html)** (`libprotobuf-mutator` / `ASAN`)
3. **[Union Type Confusion & Out-of-Order Deserialization in Embeddable Scripting VMs](https://ccsimplyspolit.github.io/writeups/vm-deserialization-union-type-confusion.html)** (`CWE-843` / Bytecode VM)
4. **[Deterministic Snapshot Fuzzing & Relocation-Aware Auditing of Binary Protocol Parsers](https://ccsimplyspolit.github.io/writeups/snapshot-fuzzing-binary-parsers.html)** (CoW Snapshots / Guard Pages)

---

## 0x02 // Open-Source Security Tooling & Research Repositories

- **[`protobuf-bounds-auditor`](https://github.com/ccsimplyspolit/protobuf-bounds-auditor)** — Static security analyzer for Protocol Buffers (`.proto`) schemas detecting unbounded `repeated` sub-messages (`CWE-1284`), unvalidated IEEE-754 `float`/`double` wire fields (`CWE-20`), and untrusted allocation lengths (`CWE-400`), with SARIF v2.1.0 output and `DEFINE_PROTO_FUZZER` harness generation (`5/5 PASS`).
- **[`cs-telemetry-internals`](https://github.com/ccsimplyspolit/cs-telemetry-internals)** — Architectural whitepapers on client-side memory page validation (`NtQueryVirtualMemory`), relocation-masked `.text` hashing, subtick protobuf telemetry, and dual-mode IDAPython/CLI static analyzer (`tools/vac_module_analyzer.py`, `3/3 PASS`).
- **[`cardinal-engine-integrity`](https://github.com/ccsimplyspolit/cardinal-engine-integrity)** — Relocation-normalized section integrity verification, IAT boundary auditing (`tools/cardinal_iat_audit.py`, `3/3 PASS`), and static classification of 4,423 simulation functions in 64-bit deterministic lockstep RTS engines.
