# Serhii Shunko (`@ccsimplyspolit`)

**Independent Systems & Binary Security Researcher**  
I audit C/C++ network and media parsers, embeddable bytecode VMs, and AI/MCP server infrastructure for memory-safety and input-validation bugs. My day-to-day work pairs static source and binary analysis with structure-aware fuzzing (`libFuzzer`, `libprotobuf-mutator`, ASan/UBSan) to turn parser state-machine edge cases into deterministic reproducers and clean upstream fixes.

- **Security Research Portal & Advisory Index:** [https://ccsimplyspolit.github.io](https://ccsimplyspolit.github.io)
- **ORCID:** [0009-0002-4183-0361](https://orcid.org/0009-0002-4183-0361)
- **CERN / Zenodo DOIs:** [`10.5281/zenodo.23641037`](https://doi.org/10.5281/zenodo.23641037) • [`10.5281/zenodo.23640494`](https://doi.org/10.5281/zenodo.23640494) • [`10.5281/zenodo.23640496`](https://doi.org/10.5281/zenodo.23640496)
- **Vulnerability Disclosure Profiles:** [HackerOne (`@sshunko`)](https://hackerone.com/sshunko) (ID Verified • Bounty Awarded) • [Bugcrowd (`@sshunko`)](https://bugcrowd.com/h/sshunko) • [Google Bug Hunters (`@sshunko`)](https://bughunters.google.com/profile/4da21a09-550c-43fe-9b62-e3e86dab4b9c)
- **Professional & Social:** [LinkedIn (`in/sshunko`)](https://www.linkedin.com/in/sshunko/) • [X (`@SergeyccShunko`)](https://x.com/SergeyccShunko)
- **Verification Dossier (PDF):** [`Serhii_Shunko_CVP_Verification_Dossier_Oct2026.pdf`](https://ccsimplyspolit.github.io/Serhii_Shunko_CVP_Verification_Dossier_Oct2026.pdf)
- **Contact & Coordinated Disclosure:** `cc.simply.spolit@gmail.com`

---

## 0x00 // Maintainer-Acknowledged Vulnerability Disclosures (CVD)

> **[CVD Policy]** Only vendor-accepted advisories, upstream-merged security fixes, and bounty-awarded disclosures are listed with full technical details below. Active reports still undergoing maintainer triage remain strictly private until upstream confirmation.

| Advisory ID | Target Component | CWE | Component Scope | Status |
| :--- | :--- | :--- | :--- | :--- |
| [`H1-4148578`](https://ccsimplyspolit.github.io/advisories/H1-4148578.html) | `brave/ai-gateway` (Brave Software) | `CWE-20` / `CWE-755` | Streaming Tool-Call Alignment Check Bypass on Multi-Tool Turns & Attachment-First User Message Extraction Failure in `OpenAIAdapter` | **Confirmed by Vendor (HackerOne `#4148578`) • Bounty Awarded (\$50.00)** |
| [`GHSA-qm7x-j9xp-x3gv`](https://ccsimplyspolit.github.io/advisories/GHSA-qm7x-j9xp-x3gv.html) | `czlonkowski/n8n-mcp` ([GHSA](https://github.com/czlonkowski/n8n-mcp/security/advisories/GHSA-qm7x-j9xp-x3gv)) | `CWE-918` / `CWE-184` | SSRF Protection Bypass in `validateUrlSync` and `validateWebhookUrl` via Trailing-Dot FQDNs and RFC 6761 `*.localhost` Subdomains (`CVSS 3.1 Low`, Defense-in-Depth) | **Confirmed & Patched in `v2.99.2` ([commit `a49dfb4`](https://github.com/czlonkowski/n8n-mcp/commit/a49dfb4))** |
| [`GHSA-cr23-59mg-h2rc`](https://ccsimplyspolit.github.io/advisories/GHSA-cr23-59mg-h2rc.html) | `bacnet-stack/bacnet-stack` ([GHSA](https://github.com/bacnet-stack/bacnet-stack/security/advisories/GHSA-cr23-59mg-h2rc)) | `CWE-125` / `CWE-787` / `CWE-400` / `CWE-835` | Pre-Auth Infinite Loop & OOB Read/Write via Negative Decode Length in `Calendar_Write_Property()` (`src/bacnet/basic/object/calendar.c`) | **Accepted by Vendor (`draft` GHSA) • [Upstream Fix PR `#1595` Open](https://github.com/bacnet-stack/bacnet-stack/pull/1595)** |
| [`GHSA-6hh9-gpj4-cr69`](https://ccsimplyspolit.github.io/advisories/GHSA-6hh9-gpj4-cr69.html) | `moonlight-stream/moonlight-common-c` ([GHSA](https://github.com/moonlight-stream/moonlight-common-c/security/advisories/GHSA-6hh9-gpj4-cr69)) | `CWE-125` / `CWE-908` | Missing `IDX_DS_ADAPTIVE_TRIGGERS` Sentinel in `packetTypesGen3..7` (`src/ControlStream.c`) | **Patched Upstream • [Fix PR `#168` Merged into `master`](https://github.com/moonlight-stream/moonlight-common-c/pull/168)** |

- **Active Coordinated Disclosure Pipeline (Under Upstream Triage):** Alongside the 4 maintainer-acknowledged disclosures above, **45** private GitHub Security Advisories (`state: triage`) and **4** active HackerOne reports—including Ruby/Onigmo (`#4148863`, where CRuby committer `@makenowjust` joined the report), Nebius AI VDP (`#4145362`), and PagerDuty/Rundeck VDP (`#4145363`, `#4145745`)—plus Bugcrowd private program research (including Cohere) remain under embargo pending maintainer review and patch release.

---

## 0x01 // Technical Methodology Write-ups

1. **[Anatomy of Unsigned Integer Underflows & Sticky-State Stack Overflows in C/C++ Parsers](https://ccsimplyspolit.github.io/writeups/integer-underflow-packet-parsers.html)** (`CWE-191` / `CWE-121`)
2. **[Structure-Aware Fuzzing of High-Frequency RPC & Simulation Protocols with libprotobuf-mutator](https://ccsimplyspolit.github.io/writeups/libprotobuf-mutator-subtick-invariants.html)** (`libprotobuf-mutator` / `ASan`)
3. **[Union Type Confusion & Out-of-Order Deserialization in Embeddable Scripting VMs](https://ccsimplyspolit.github.io/writeups/vm-deserialization-union-type-confusion.html)** (`CWE-843` / Bytecode VM)
4. **[Deterministic Snapshot Fuzzing & Relocation-Aware Auditing of Binary Protocol Parsers](https://ccsimplyspolit.github.io/writeups/snapshot-fuzzing-binary-parsers.html)** (CoW Snapshots / Guard Pages)

---

## 0x02 // Open-Source Security Tooling & Published Research (CERN / Zenodo DOIs)

- **[`protobuf-bounds-auditor`](https://github.com/ccsimplyspolit/protobuf-bounds-auditor)** ([`DOI: 10.5281/zenodo.23641037`](https://doi.org/10.5281/zenodo.23641037)) — Static security analyzer for Protocol Buffers (`.proto`) schemas detecting unbounded `repeated` sub-messages (`CWE-1284`), unvalidated IEEE-754 `float`/`double` wire fields (`CWE-20`), and untrusted allocation lengths (`CWE-400`), with SARIF v2.1.0 output and `DEFINE_PROTO_FUZZER` harness generation (`5/5 PASS`).
- **[`cs-telemetry-internals`](https://github.com/ccsimplyspolit/cs-telemetry-internals)** ([`DOI: 10.5281/zenodo.23640494`](https://doi.org/10.5281/zenodo.23640494)) — Six technical whitepapers and static analyzer covering server-side Protocol Buffers wire input validation, IEEE-754 `NaN`/`Inf` sanitization, and relocation-masked PE32+ `.text` section integrity verification (`3/3 PASS`).
- **[`cardinal-engine-integrity`](https://github.com/ccsimplyspolit/cardinal-engine-integrity)** ([`DOI: 10.5281/zenodo.23640496`](https://doi.org/10.5281/zenodo.23640496)) — Four architectural whitepapers and zero-dependency PE32+ static auditor covering relocation-normalized section integrity verification, Import Address Table (IAT) boundary auditing (`3/3 PASS`), and static classification of 4,423 deterministic simulation functions.
