# Serhii Shunko (`@sshunko` / `@ccsimplyspolit`)

**Independent Systems & Binary Security Researcher**  
Focus: C/C++ Memory Safety, Binary Protocol Fuzzing (`libFuzzer` / `libprotobuf-mutator` / ASAN), Virtual Machine Deserialization Internals, and AI/MCP Infrastructure Security.

- **Security Research Portal & Advisory Index:** [https://ccsimplyspolit.github.io](https://ccsimplyspolit.github.io)
- **ORCID:** [0009-0002-4183-0361](https://orcid.org/0009-0002-4183-0361)
- **GitHub:** [@ccsimplyspolit](https://github.com/ccsimplyspolit)
- **HackerOne:** [https://hackerone.com/sshunko](https://hackerone.com/sshunko)
- **Contact & Coordinated Disclosure:** `cc.simply.spolit@gmail.com`

---

## 0x01 // Confirmed Vulnerability Disclosures & Published Specifications

> **[CVD Policy]** Only vendor-accepted advisories, bounty-awarded disclosures, and published technical specifications are listed below. Active reports still undergoing initial maintainer triage remain strictly private until upstream confirmation.

| Advisory ID | Target Component | CWE | Component Scope | Status |
| :--- | :--- | :--- | :--- | :--- |
| [`GHSA-cr23-59mg-h2rc`](https://ccsimplyspolit.github.io/advisories/GHSA-cr23-59mg-h2rc.html) | `bacnet-stack/bacnet-stack` | `CWE-125 / CWE-400 / CWE-787` | Pre-Auth Infinite Loop / Heap Exhaustion and Out-of-Bounds Read/Write via Unchecked Negative Decode Lengths in `Calendar_Write_Property()` and `Notification_Class_Write_Property()` | **Accepted (GHSA Draft — [Fix PR #1595](https://github.com/bacnet-stack/bacnet-stack/pull/1595))** |
| [`H1-4148578`](https://ccsimplyspolit.github.io/advisories/H1-4148578.html) | `brave/ai-gateway` | `CWE-20 / CWE-755` | Multi-Tool Call Buffer State Desynchronization and Unhandled Validation Exceptions in `OpenAIAdapter` Streaming Tool Parser | **Confirmed & Bounty Awarded (HackerOne `#4148578`)** |
| [`ADV-2026-003`](https://github.com/ccsimplyspolit/cs-telemetry-internals/blob/main/advisories/api_security_audits/ADV-2026-003_ssrf_case_url_audit.md) | `Replay Ingestion Workers` | `CWE-918` | Post-resolution IP allowlisting and DNS-rebinding defenses for asynchronous replay-ingestion pipelines. | **Published Specification** |
| [`ADV-2026-004`](https://github.com/ccsimplyspolit/cs-telemetry-internals/blob/main/advisories/api_security_audits/ADV-2026-004_key_value_injection_audit.md) | `VDF / KeyValues Parsers` | `CWE-943 / CWE-674` | Delimiter breakout, stack exhaustion, and Unicode digit normalization in VDF/KeyValues deserializers. | **Published Specification** |
| [`ADV-2026-005`](https://github.com/ccsimplyspolit/cs-telemetry-internals/blob/main/advisories/api_security_audits/ADV-2026-005_openid_replay_mitigation.md) | `OpenID 2.0 Relying Parties` | `CWE-290 / CWE-294` | Strict `openid.op_endpoint` pinning and cryptographic nonce consumption in stateless Relying Parties. | **Published Specification** |

---

## 0x02 // Open-Source Defensive Tooling & Binary Research

- **[`protobuf-bounds-auditor`](https://github.com/ccsimplyspolit/protobuf-bounds-auditor)** — Static security analyzer for Protocol Buffers (`.proto`) schemas detecting unbounded `repeated` sub-messages (`CWE-1284`), unvalidated IEEE-754 `float`/`double` wire fields (`CWE-20`), and untrusted allocation lengths (`CWE-400`), with SARIF v2.1.0 output and `DEFINE_PROTO_FUZZER` harness generation.
- **[`cs-telemetry-internals`](https://github.com/ccsimplyspolit/cs-telemetry-internals)** — Architectural analysis of client-side memory page validation (`NtQueryVirtualMemory`), relocation-masked `.text` hashing, and defensive specifications for replay-ingestion SSRF (`ADV-2026-003`), VDF/KeyValues injection (`ADV-2026-004`), and OpenID 2.0 relying-party verification (`ADV-2026-005`).
- **[`cardinal-engine-integrity`](https://github.com/ccsimplyspolit/cardinal-engine-integrity)** — Relocation-normalized section integrity verification, IAT boundary auditing, and static classification of 4,423 simulation functions in 64-bit deterministic lockstep RTS engines (`ADV-2026-002`).

---

## 0x03 // Technical Methodology Write-ups

1. **[Anatomy of Unsigned Integer Underflows & Sticky-State Stack Overflows in C/C++ Parsers](https://ccsimplyspolit.github.io/writeups/integer-underflow-packet-parsers.html)** (`CWE-191` / `CWE-121`)
2. **[Structure-Aware Fuzzing of High-Frequency RPC & Simulation Protocols with libprotobuf-mutator](https://ccsimplyspolit.github.io/writeups/libprotobuf-mutator-subtick-invariants.html)** (`libprotobuf-mutator` / `ASAN`)
3. **[Union Type Confusion & Out-of-Order Deserialization in Embeddable Scripting VMs](https://ccsimplyspolit.github.io/writeups/vm-deserialization-union-type-confusion.html)** (`CWE-843` / Bytecode VM)
4. **[Deterministic Snapshot Fuzzing & Relocation-Aware Auditing of Binary Protocol Parsers](https://ccsimplyspolit.github.io/writeups/snapshot-fuzzing-binary-parsers.html)** (CoW Snapshots / Guard Pages)
