# Serhii Shunko (`sshunko`) — Application & Binary Security Research

**Independent Security Researcher | Protocol Input Validation, Static Binary Auditing & Defensive Engineering**

- **Security Research Portal:** [https://ccsimplyspolit.github.io](https://ccsimplyspolit.github.io)
- **ORCID:** [`0009-0002-4183-0361`](https://orcid.org/0009-0002-4183-0361) | **Education:** B.Sc. in Applied Mathematics & Software Engineering (Oles Honchar Dnipro National University)
- **Verified Researcher Profiles (`@sshunko`):** [HackerOne (`@sshunko` — ID Verified)](https://hackerone.com/sshunko) · [Bugcrowd (`@sshunko`)](https://bugcrowd.com/h/sshunko) · [Intigriti (`@sshunko`)](https://app.intigriti.com/profile/sshunko) · [Google Bug Hunters (`@sshunko`)](https://bughunters.google.com/profile/4da21a09-550c-43fe-9b62-e3e86dab4b9c) · [Immunefi (`@sshunko`)](https://immunefi.com/profile/sshunko) · [pwn.college (`@sshunko` / `#247319`)](https://pwn.college/hacker/247319) · [HexTree.io (`@sshunko`)](https://app.hextree.io/profile/simple-loop-block) · [Crackmes.one (`@sshunko`)](https://crackmes.one/user/sshunko) · [CTFtime (`@sshunko` / `#277345`)](https://ctftime.org/user/277345) · [Huntr (`@ccsimplyspolit`)](https://huntr.com/users/ccsimplyspolit) · [LinkedIn (`@sshunko`)](https://www.linkedin.com/in/sshunko)
- **Focus Areas:** Server-side deserialization security (Protobuf / RPC / KLV / VDF), static disassembly & decompilation (`x86_64` PE / ELF), deterministic simulation state verification, and memory-safety vulnerability discovery (`ASAN` / `LibFuzzer`).
- **Coordinated Vulnerability Disclosure (CVD) Embargo Policy:** Active vulnerability reports currently in vendor triage (`GHSA-*` and `CVD-2026-*`) are listed by identifier, CWE classification, and high-level component scope only. Full technical write-ups, reproduction harnesses, and remediation diffs are withheld until upstream patches are released.

---

## Coordinated Vulnerability Disclosures & Security Advisories

| ID | Target / Component | Vulnerability Class & Scope (Embargo Summary) | Status / Reference |
|---|---|---|---|
| **GHSA-48q7-428c-jmfw** | `Graphify-Labs/graphify` | Preprocessor Directive Filtering &amp; SSRF Address Validation (`CWE-184 / CWE-200 / CWE-918 (High 7.5)`) | `Embargoed — In Vendor Triage (GitHub CNA)` |
| **GHSA-mxjx-wqmx-hwx7** | `HKUDS/nanobot` | SSRF Address Normalization &amp; Workspace Boundary Enforcement (`CWE-918 / CWE-184 / CWE-22 (High 8.2)`) | `Embargoed — In Vendor Triage (GitHub CNA)` |
| **GHSA-gx9q-44qw-3frv** | `DeusData/codebase-memory-mcp` | Stack Buffer Termination &amp; XML Serializer Bounds (`CWE-170 / CWE-125 (High 7.1)`) | `Embargoed — In Vendor Triage (GitHub CNA)` |
| **GHSA-j47j-8qq9-628m** | `gopro/gpmf-parser` | Stack Buffer Bounds &amp; Nesting Depth Validation in KLV Telemetry Parser (`CWE-121 / CWE-787 (High 8.8)`) | `Embargoed — In Vendor Triage (GitHub CNA)` |
| **GHSA-4xx2-wr42-gjg3** | `meshcore-dev/MeshCore` | Unsigned Length Arithmetic &amp; Frame Bounds Validation (`CWE-191 / CWE-125 (High 8.2)`) | `Embargoed — In Vendor Triage (GitHub CNA)` |
| **GHSA-6hh9-gpj4-cr69** | `moonlight-stream/moonlight-common-c` | Dispatch Table Bounds &amp; Buffer Initialization (`CWE-125 / CWE-908 (Medium 6.5)`) | `Embargoed — In Vendor Triage (GitHub CNA)` |
| **GHSA-g278-chr4-fg9f** | `marcobambini/gravity` | Tagged-Union Deserialization Invariants &amp; Array Length Validation (`CWE-843 / CWE-125 (High 8.6)`) | `Embargoed — In Vendor Triage (GitHub CNA)` |
| **GHSA-wf26-5m35-vf27** | `lief-project/LIEF` | Binary Section Offset Bounds &amp; Type Parser Recursion Depth (`CWE-787 / CWE-674 (High 8.8)`) | `Embargoed — In Vendor Triage (GitHub CNA)` |
| **GHSA-cr23-59mg-h2rc** | `bacnet-stack/bacnet-stack` | Property Decoding Loop Termination &amp; Buffer Length Tracking (`CWE-835 / CWE-125 (High 8.2)`) | `Embargoed — In Vendor Triage (GitHub CNA)` |
| **GHSA-7m49-w797-wqp6** | `pocketpy/pocketpy` | Binary Deserializer Stack/Heap Bounds &amp; Value Type Validation (`CWE-121 / CWE-787 (Critical 9.8)`) | `Embargoed — In Vendor Triage (GitHub CNA)` |
| **CVD-2026-CS2-001** | `Source 2 Dedicated Server` | Repeated Sub-Message Cardinality &amp; Input Domain Validation (`CWE-20 / CWE-1284 (High 7.1)`) | `Embargoed — In Vendor Triage` |
| **CVD-2026-CS2-003** | `Source 2 Dedicated Server` | IEEE-754 View-Angle Domain Clamping Invariants (`CWE-20 / CWE-682 (High 7.1)`) | `Embargoed — In Vendor Triage` |
| **CVD-2026-CS2-002** | `Source 2 Dedicated Server` | Subtick Fractional Timestamp Monotonicity Validation (`CWE-20 / CWE-841 (Medium 5.3)`) | `Embargoed — In Vendor Triage` |
| **CVD-2026-SSRF-001** | `arkadiyt/ssrf_filter` | Multi-Hop Redirect Origin Tracking &amp; IPv6 Prefix Validation (`CWE-918 / CWE-200 (Medium 6.5)`) | `Embargoed — In Vendor Triage` |
| **CVD-2026-SUPA-001** | `supabase-community/supabase-mcp` | SQL Tokenizer State-Machine Validation (`CWE-184 / CWE-436 (Medium 6.5)`) | `Embargoed — In Vendor Triage` |
| **CVD-2026-TOMTOM-001** | `tomtom-international/tomtom-maps-mcp` | Authentication Header Precedence &amp; URL Validation (`CWE-287 / CWE-918 (High 7.5)`) | `Embargoed — In Vendor Triage` |
| **CVD-2026-GNS-001** | `ValveSoftware/GameNetworkingSockets` | Encoder Length Arithmetic &amp; 64-Bit Offset Bounds (`CWE-191 / CWE-190 (High 7.5)`) | `Embargoed — In Vendor Triage` |
| **CVD-2026-ONNX-001** | `onnx/onnx` | Post-Parse External Tensor Path &amp; Descriptor Validation (`CWE-20 / CWE-22 (High 7.5)`) | `Embargoed — In Vendor Triage` |
| **CVD-2026-LLAMA-001** | `ggml-org/llama.cpp` | RPC Tensor Deserialization Bounds &amp; 64-Bit Offset Arithmetic (`CWE-190 / CWE-787 (High 8.1)`) | `Embargoed — In Vendor Triage` |
| **CVD-2026-STRANDS-001** | `strands-agents/sdk-python` | Compound shell command composition and argument delimiter handling in sandbox execution helpers. (`CWE-78 / CWE-88`) | `Embargoed (Vendor Triage)` |
| **CVD-2026-NEBIUS-001** | `nebius/mcp-server & nebius/contree-mcp` | CLI argument filter normalization, cache exclusion path matching, and registry redirect handling. (`CWE-184 / CWE-200 / CWE-319`) | `Embargoed (Vendor Triage)` |
| **CVD-2026-OMARCHY-001** | `basecamp/omarchy` | URI host string escaping in window-manager dispatch scripts and temporary directory ownership checks. (`CWE-78 / CWE-59`) | `Embargoed (Vendor Triage)` |
| **CVD-2026-CHIA-001** | `Chia-Network/chia-blockchain` | DataLayer plugin store grouping validation and upload verification invariants. (`CWE-20 / CWE-345`) | `Embargoed (Vendor Triage)` |
| **CVD-2026-CAO-001** | `awslabs/cli-agent-orchestrator` | Filesystem symlink canonicalization and ancestor path blocklist validation on macOS/POSIX. (`CWE-59 / CWE-22`) | `Embargoed (Vendor Triage)` |
| **CVD-2026-DJL-001** | `deepjavalibrary/djl-serving` | Dynamic model and adapter URI allowlist enforcement across HTTP request property sources. (`CWE-863 / CWE-20 / CWE-918`) | `Embargoed (Vendor Triage)` |
| **CVD-2026-SUPAMCP-002** | `supabase/mcp` | SQL statement classification and confirmation guard parsing for complex query structures. (`CWE-863 / CWE-20`) | `Embargoed (Vendor Triage)` |
| **CVD-2026-RAILS-001** | `rails/rails` | Malformed header exception handling and constant-response behavior in HTTP authentication middlewares. (`CWE-755 / CWE-203`) | `Embargoed (Vendor Triage)` |
| **CVD-2026-CURL-001** | `curl/curl` | TLS session ticket deserialization invariants, error-path allocation cleanup, and signed/unsigned return handling. (`CWE-617 / CWE-401 / CWE-195`) | `Embargoed (Vendor Triage)` |
| **CVD-2026-INGRESSNGINX-001** | `kubernetes/ingress-nginx` | Annotation regex anchoring and fail-closed default enforcement in ingress configuration validators. (`CWE-185 / CWE-942 / CWE-636`) | `Embargoed (Vendor Triage)` |
| **CVD-2026-CPYTHON-001** | `python/cpython` | Integer attribute validation in HTTP cookie parsing and truncated binary catalog bounds checks. (`CWE-20 / CWE-755`) | `Embargoed (Vendor Triage)` |
| **CVD-2026-PHP-001** | `php/php-src` | Cross-origin port comparison and error-path URI buffer cleanup in HTTP redirect handling. (`CWE-601 / CWE-200 / CWE-401`) | `Embargoed (Vendor Triage)` |
| **CVD-2026-REDIS-001** | `redis/redis` | Integer width preservation and unsigned length bounds checking in binary cluster packet extensions. (`CWE-681 / CWE-191 / CWE-125`) | `Embargoed (Vendor Triage)` |
| **CVD-2026-GOOSE-001** | `block/goose` | Workspace directory path containment and fail-closed authorization list parsing in gateway handlers. (`CWE-22 / CWE-284 / CWE-863`) | `Embargoed (Vendor Triage)` |
| **CVD-2026-CLOUDFLARE-MCP-001** | `cloudflare/mcp-server-cloudflare` | URI scheme allowlisting and consent state validation in OAuth authorization helpers. (`CWE-79 / CWE-20 / CWE-863`) | `Embargoed (Vendor Triage)` |
| **CVD-2026-MATTERMOST-AI-001** | `mattermost/mattermost-plugin-ai` | Attachment channel authorization and caller identity verification in bridge message handlers. (`CWE-862 / CWE-863 / CWE-400`) | `Embargoed (Vendor Triage)` |
| **CVD-2026-GHMCP-001** | `github/github-mcp-server` | State parameter verification ordering in loopback OAuth callback servers. (`CWE-352 / CWE-400`) | `Embargoed (Vendor Triage)` |
| **CVD-2026-GRAFANA-MCP-001** | `grafana/mcp-grafana` | AST matcher complexity analysis and range duration parsing in query policy guards. (`CWE-185 / CWE-20 / CWE-400`) | `Embargoed (Vendor Triage)` |
| **CVD-2026-NODE-001** | `nodejs/node` | Prefix tree wildcard matching and directory boundary normalization in filesystem permission checks. (`CWE-285 / CWE-863`) | `Embargoed (Vendor Triage)` |
| **CVD-2026-RUBY-001** | `ruby/ruby` | Zero-repetition quantifier compilation invariants in regular expression bytecode generation. (`CWE-1333 / CWE-755`) | `Embargoed (Vendor Triage)` |
| **CVD-2026-RUNDECK-002** | `rundeck/rundeck` | Storage reference path canonicalization and project ownership verification during job import. (`CWE-22 / CWE-73 / CWE-639`) | `Embargoed (Vendor Triage)` |
| **CVD-2026-RUNDECK-001** | `rundeck/mcp` | Origin validation for authenticated API requests and path normalization in confirmation guards. (`CWE-918 / CWE-522 / CWE-863`) | `Embargoed (Vendor Triage)` |
| **ADV-2026-001** | Windows x64 Endpoint Integrity Subsystems | Architecture of Client-Side Memory Page Validation & Heuristic Telemetry Reporting | [Published Specification](https://github.com/ccsimplyspolit/cs-telemetry-internals/blob/main/advisories/ADV-2026-001_memory_scanning_telemetry.md) |
| **ADV-2026-002** | Cardinal Engine (`RelicCardinal.exe` x64) | Relocation-Masked Section Integrity, IAT Boundary Auditing & Deterministic State Synchronization | [Published Specification](https://github.com/ccsimplyspolit/cardinal-engine-integrity/blob/main/advisories/ADV-2026-002_anti_tamper_mechanics.md) |
| **ADV-2026-003** | Replay & Telemetry Ingestion Workers | Server-Side Request Forgery (`CWE-918`) & URL Parser Confusion in Asynchronous Replay Fetching | [Published Specification](https://github.com/ccsimplyspolit/cs-telemetry-internals/blob/main/advisories/api_security_audits/ADV-2026-003_ssrf_case_url_audit.md) |
| **ADV-2026-004** | VDF / KeyValues Deserializers | Structural KeyValues Injection (`CWE-943`) & Unbounded Recursive Descent Exhaustion (`CWE-674`) | [Published Specification](https://github.com/ccsimplyspolit/cs-telemetry-internals/blob/main/advisories/api_security_audits/ADV-2026-004_key_value_injection_audit.md) |
| **ADV-2026-005** | Custom OpenID 2.0 Relying Parties | Authentication Bypass (`CWE-290`) & Assertion Replay (`CWE-294`) in OpenID 2.0 Callback Verifiers | [Published Specification](https://github.com/ccsimplyspolit/cs-telemetry-internals/blob/main/advisories/api_security_audits/ADV-2026-005_openid_replay_mitigation.md) |

---

## Primary Research Repositories & Archival DOIs (CERN / Zenodo)

- **[`ccsimplyspolit/cs-telemetry-internals`](https://github.com/ccsimplyspolit/cs-telemetry-internals)** [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23640494.svg)](https://doi.org/10.5281/zenodo.23640494) — Server-side Protobuf input validation specifications, subtick false-positive mitigation models, and Windows x64 memory verification architecture (`DOI: 10.5281/zenodo.23640494`).
- **[`ccsimplyspolit/cardinal-engine-integrity`](https://github.com/ccsimplyspolit/cardinal-engine-integrity)** [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23640496.svg)](https://doi.org/10.5281/zenodo.23640496) — Relocation-normalized `.text` section hashing, IAT boundary verification, PE header reconstruction, and a 4,423-function deterministic lockstep simulation state audit (`DOI: 10.5281/zenodo.23640496`).
- **[`ccsimplyspolit/protobuf-bounds-auditor`](https://github.com/ccsimplyspolit/protobuf-bounds-auditor)** [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23640498.svg)](https://doi.org/10.5281/zenodo.23640498) — Static security analyzer (`proto_audit.py` v1.1.0) for Protocol Buffers (`.proto`) schemas detecting `CWE-1284` unbounded repeated fields, `CWE-20` unvalidated IEEE-754 float/double inputs, and `CWE-400` untrusted allocation sizes with SARIF v2.1.0 output and `libprotobuf-mutator` `DEFINE_PROTO_FUZZER` harness generation (`DOI: 10.5281/zenodo.23640498`).
- **[`ccsimplyspolit/ccsimplyspolit.github.io`](https://github.com/ccsimplyspolit/ccsimplyspolit.github.io)** — Public Security Research Portal hosting the Coordinated Vulnerability Disclosure (CVD) registry (with full technical details withheld during active vendor triage embargoes) and defensive methodology write-ups.

---

## Methodology Write-ups

- **[Anatomy of Unsigned Integer Underflows & Sticky-State Stack Overflows in C/C++ Parsers](https://ccsimplyspolit.github.io/writeups/integer-underflow-packet-parsers.html)** — Two-pass validation mismatches, narrow unsigned remainder wraparound (`CWE-191`), and cross-record calibration state bounds (`CWE-121`).
- **[Structure-Aware Fuzzing of High-Frequency RPC & Simulation Protocols with libprotobuf-mutator](https://ccsimplyspolit.github.io/writeups/libprotobuf-mutator-subtick-invariants.html)** — Static `.proto` auditing (`protobuf-bounds-auditor v1.1.0`), automated `DEFINE_PROTO_FUZZER` C++ harness generation, and post-parse external descriptor invariants.
- **[Union Type Confusion & Out-of-Order Deserialization in Embeddable Scripting VMs](https://ccsimplyspolit.github.io/writeups/vm-deserialization-union-type-confusion.html)** — Tagged-union memory aliasing (`CWE-843`), out-of-order key-value deserialization, and signed LEB128 count validation in C virtual machines.
- **[Deterministic Snapshot Fuzzing & Relocation-Aware Auditing of Binary Protocol Parsers](https://ccsimplyspolit.github.io/writeups/snapshot-fuzzing-binary-parsers.html)** — Copy-on-Write (CoW) dirty-page rollback, page-aligned guard allocations, and overflow-safe 64-bit pointer offset verification.
