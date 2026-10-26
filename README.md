# Serhii Shunko (`@sshunko` / `@ccsimplyspolit`)

**Independent Systems & Binary Security Researcher**  
Focus: C/C++ Memory Safety, Binary Protocol Fuzzing (`libFuzzer` / `libprotobuf-mutator` / ASAN), Virtual Machine Deserialization Internals, and AI/MCP Infrastructure Security.

- **Security Research Portal & Advisory Index:** [https://ccsimplyspolit.github.io](https://ccsimplyspolit.github.io)
- **ORCID:** [0009-0002-4183-0361](https://orcid.org/0009-0002-4183-0361)
- **GitHub:** [@ccsimplyspolit](https://github.com/ccsimplyspolit)
- **HackerOne:** [https://hackerone.com/sshunko](https://hackerone.com/sshunko)
- **Contact & Coordinated Disclosure:** `sshunko@gmail.com`

---

## 0x01 // Coordinated Vulnerability Disclosure (CVD) & Active Advisories

> **[CVD Embargo Policy]** Active vendor-specific findings are maintained under strict coordinated vulnerability disclosure embargo while upstream maintainers complete triage and patch release. Public verification records publish only the identifier, CWE classification, high-level component scope, and SHA-256 cryptographic commitment hash (`specification_sha256_commitment`). Full proof-of-concept harnesses and remediation diffs are restricted to vendor security teams via GitHub Private Vulnerability Reporting (`GHSA-*`) and HackerOne.

| Advisory ID | Target Component | CWE | Component Scope (Embargo Summary) | Status |
| :--- | :--- | :--- | :--- | :--- |
| [`GHSA-48q7-428c-jmfw`](https://ccsimplyspolit.github.io/advisories/GHSA-48q7-428c-jmfw.html) | `Graphify-Labs/graphify` | `CWE-184 / CWE-200 / CWE-918` | Incomplete Fix for GHSA-pcc4-rvhr-2pr8 in Fortran Preprocessor Filter (graphify/extractors/fortran.py) and IPv6/Redirect SSRF Bypass (graphify/security.py, graphify/transcribe.py) | **In Triage (GHSA)** |
| [`GHSA-mxjx-wqmx-hwx7`](https://ccsimplyspolit.github.io/advisories/GHSA-mxjx-wqmx-hwx7.html) | `HKUDS/nanobot` | `CWE-22 / CWE-184 / CWE-918` | Incomplete Fix for GHSA-vc5v-6vwm-wf9m (ZDI-CAN-29369) in nanobot/security/network.py and Command/Path Guard Bypass in nanobot/agent/tools/shell.py | **In Triage (GHSA)** |
| [`GHSA-gx9q-44qw-3frv`](https://ccsimplyspolit.github.io/advisories/GHSA-gx9q-44qw-3frv.html) | `DeusData/codebase-memory-mcp` | `CWE-125 / CWE-170` | Out-of-Bounds Stack Read via Non-Null-Terminated strncpy in emit_property() (CWE-170 / CWE-125) and Unchecked Pointer Subtraction in extract_attr() (internal/cbm/iris_export_xml.c) | **In Triage (GHSA)** |
| [`GHSA-wf26-5m35-vf27`](https://ccsimplyspolit.github.io/advisories/GHSA-wf26-5m35-vf27.html) | `lief-project/LIEF` | `CWE-125 / CWE-190 / CWE-674` | Heap Buffer Overflow (CWE-787) in ELF::Segment::set_content_value and Unbounded Recursion / Heap OOB Read-Write in DEX/VDEX Parsers | **In Triage (GHSA)** |
| [`GHSA-cr23-59mg-h2rc`](https://ccsimplyspolit.github.io/advisories/GHSA-cr23-59mg-h2rc.html) | `bacnet-stack/bacnet-stack` | `CWE-125 / CWE-400 / CWE-787` | Pre-Auth Infinite Loop / Heap Exhaustion (CWE-835 / CWE-400) and Out-of-Bounds Read (CWE-125) in Calendar_Write_Property() and Notification_Class_Write_Property() | **Accepted (GHSA Draft — Fix PR #1595)** |
| [`GHSA-7m49-w797-wqp6`](https://ccsimplyspolit.github.io/advisories/GHSA-7m49-w797-wqp6.html) | `pocketpy/pocketpy` | `CWE-121 / CWE-125 / CWE-787` | Stack-Based Buffer Overflow (CWE-121), Out-of-Bounds Memo Read/Write (CWE-787), and Raw Pointer Forgery (CWE-822) in pickle.loads() (src/modules/pickle.c) | **In Triage (GHSA)** |
| [`GHSA-g278-chr4-fg9f`](https://ccsimplyspolit.github.io/advisories/GHSA-g278-chr4-fg9f.html) | `marcobambini/gravity` | `CWE-125 / CWE-843` | Union Type Confusion (CWE-843) and Heap Buffer Over-Read (CWE-125) in gravity_function_deserialize() | **In Triage (GHSA)** |
| [`GHSA-j47j-8qq9-628m`](https://ccsimplyspolit.github.io/advisories/GHSA-j47j-8qq9-628m.html) | `gopro/gpmf-parser` | `CWE-121 / CWE-191 / CWE-193` | Stack-Based Buffer Overflow in GPMF_ScaledData() via Unbounded ORIN/ORIO Calibration Matrix Generation (CWE-121 / CWE-787) | **In Triage (GHSA)** |
| [`GHSA-4xx2-wr42-gjg3`](https://ccsimplyspolit.github.io/advisories/GHSA-4xx2-wr42-gjg3.html) | `meshcore-dev/MeshCore` | `CWE-125 / CWE-191` | Unsigned Integer Underflow (CWE-191) and Out-of-Bounds Read (CWE-125) in Mesh::onRecvPacket() and Packet::readFrom() | **In Triage (GHSA)** |
| [`GHSA-6hh9-gpj4-cr69`](https://ccsimplyspolit.github.io/advisories/GHSA-6hh9-gpj4-cr69.html) | `moonlight-stream/moonlight-common-c` | `CWE-125 / CWE-908` | Out-of-Bounds Read (CWE-125) and Uninitialized Memory Usage (CWE-908) in ControlStream Packet Dispatch (src/ControlStream.c) | **In Triage (GHSA)** |
| [`GHSA-hfc6-f2q5-m256`](https://ccsimplyspolit.github.io/advisories/GHSA-hfc6-f2q5-m256.html) | `tinyhumansai/openhuman` | `CWE-22 / CWE-78 / CWE-863` | Shell Protected-Path Floor and Read-Only Classifier Bypass via Intra-Word Quote Splitting, file:// URLs, and git --output in CommandAnalysis | **In Triage (GHSA)** |
| [`GHSA-ggvf-5fq9-jxq2`](https://ccsimplyspolit.github.io/advisories/GHSA-ggvf-5fq9-jxq2.html) | `rtk-ai/rtk` | `CWE-22 / CWE-345 / CWE-829` | Project Pipeline Trust Gate Bypass via RTK_CONFIG_DIR Override and Un-Hashed External Directive File Targets | **In Triage (GHSA)** |
| [`GHSA-qm7x-j9xp-x3gv`](https://ccsimplyspolit.github.io/advisories/GHSA-qm7x-j9xp-x3gv.html) | `czlonkowski/n8n-mcp` | `CWE-184 / CWE-918` | SSRF Protection Bypass in validateUrlSync and validateWebhookUrl via Trailing-Dot FQDNs and RFC 6761 *.localhost Subdomains | **In Triage (GHSA)** |
| [`GHSA-7mfv-3jjj-45vr`](https://ccsimplyspolit.github.io/advisories/GHSA-7mfv-3jjj-45vr.html) | `colbymchenry/codegraph` | `CWE-20 / CWE-78` | Unvalidated Version Tag Interpolation in PowerShell Upgrade Script and Windows cmd.exe Invocation in src/upgrade/index.ts | **In Triage (GHSA)** |
| [`GHSA-2qf6-94w7-mjcq`](https://ccsimplyspolit.github.io/advisories/GHSA-2qf6-94w7-mjcq.html) | `onnx/onnx` | `CWE-22 / CWE-367 / CWE-755` | External Data #-Prefix Path/Size Check Bypass, Missing Post-Open S_ISREG Check, and Uncaught Numeric Parser Exceptions | **In Triage (GHSA)** |
| [`GHSA-h3mc-v47q-wj82`](https://ccsimplyspolit.github.io/advisories/GHSA-h3mc-v47q-wj82.html) | `ValveSoftware/GameNetworkingSockets` | `CWE-125 / CWE-190 / CWE-191` | Unbounded 64-Bit Unreliable Message Number Offset, Zero-Length Segment OOB Read, Base64EncodeMaxOutput(0) Underflow, and CUtlBuffer::GetString Seek Misalignment | **In Triage (GHSA)** |
| [`GHSA-rg4w-8g8x-2vhf`](https://ccsimplyspolit.github.io/advisories/GHSA-rg4w-8g8x-2vhf.html) | `github/github-mcp-server` | `CWE-352 / CWE-400` | OAuth PKCE Callback Server Single-Shot Channel Exhaustion Before state Validation in internal/oauth/callback.go | **In Triage (GHSA)** |
| [`GHSA-29j7-mxxj-g9hg`](https://ccsimplyspolit.github.io/advisories/GHSA-29j7-mxxj-g9hg.html) | `cloudflare/mcp-server-cloudflare` | `CWE-20 / CWE-79 / CWE-863` | Unvalidated clientUri Scheme in OAuth Approval Dialog and Fail-Open Consent Decision Parsing in workers-oauth-utils.ts | **In Triage (GHSA)** |
| [`GHSA-g4pg-rg2m-6vm4`](https://ccsimplyspolit.github.io/advisories/GHSA-g4pg-rg2m-6vm4.html) | `paypal/agent-toolkit` | `CWE-20 / CWE-22 / CWE-285` | paypal/agent-toolkit: Resource identifier validation and URL path segment encoding in REST tool handlers | **In Triage (GHSA)** |
| [`GHSA-x2gm-fvv7-8x97`](https://ccsimplyspolit.github.io/advisories/GHSA-x2gm-fvv7-8x97.html) | `stytchauth/samlshield` | `CWE-20 / CWE-287` | stytchauth/samlshield: Timestamp NaN validation and subject element cardinality checks in SAML assertion verification | **In Triage (GHSA)** |
| `CVD-2026-NEBIUS-001` | `nebius/mcp-server & nebius/contree-mcp` | `CWE-88 / CWE-22 / CWE-200` | CLI option delimiter handling, symlink/prefix cache exclusion checks, and cross-origin redirect header stripping (H1 #4145362). | **Embargoed (Vendor Triage)** |
| `CVD-2026-RUNDECK-001` | `rundeck/mcp` | `CWE-918 / CWE-522 / CWE-863` | Origin validation for authenticated API requests and path normalization in confirmation guards (H1 #4145363). | **Embargoed (Vendor Triage)** |
| `CVD-2026-RUNDECK-002` | `rundeck/rundeck` | `CWE-22 / CWE-73 / CWE-639` | Storage reference path canonicalization and project ownership verification during job import (H1 #4145745). | **Embargoed (Vendor Triage)** |
| `CVD-2026-RUBY-001` | `ruby/ruby` | `CWE-1333 / CWE-755` | Zero-repetition quantifier compilation invariants in regular expression bytecode generation (H1 #4145826). | **Embargoed (Vendor Triage)** |
| `CVD-2026-NODE-001` | `nodejs/node` | `CWE-285 / CWE-863` | Prefix tree wildcard matching and directory boundary normalization in filesystem permission checks (H1 #4145962). | **Embargoed (Vendor Triage)** |
| [`CVD-2026-CREWAI-MEM-001`](https://ccsimplyspolit.github.io/advisories/CVD-2026-CREWAI-MEM-001.html) | `crewAIInc/crewAI` | `CWE-328 / CWE-639 / CWE-59` | Point ID hashing, scope filter enforcement during record deletion, and symlink validation in edge shard storage. | **Embargoed (Vendor Triage)** |
| [`CVD-2026-GHAW-CORE-001`](https://ccsimplyspolit.github.io/advisories/CVD-2026-GHAW-CORE-001.html) | `github/gh-aw` | `CWE-377 / CWE-59 / CWE-732` | Exclusive temporary file creation and permission mode preservation in CLI compilation progress writers. | **Embargoed (Vendor Triage)** |
| `CVD-2026-PHP-001` | `php/php-src` | `CWE-200 / CWE-918` | Cross-origin port comparison and credential header stripping across HTTP redirects in SOAP client transport. | **Embargoed (Vendor Triage)** |
| `CVD-2026-CPYTHON-001` | `python/cpython` | `CWE-20 / CWE-284` | Cookie policy domain/path matching invariants and catalog expression validation in standard library modules. | **Embargoed (Vendor Triage)** |
| [`CVD-2026-GHAW-FW-001`](https://ccsimplyspolit.github.io/advisories/CVD-2026-GHAW-FW-001.html) | `github/gh-aw-firewall` | `CWE-59 / CWE-732` | Non-symlink ownership changes in chroot initialization and target path validation in container audit preservation. | **Embargoed (Vendor Triage)** |
| [`CVD-2026-HF-MCP-001`](https://ccsimplyspolit.github.io/advisories/CVD-2026-HF-MCP-001.html) | `huggingface/hf-mcp-server` | `CWE-22 / CWE-918 / CWE-200` | Path segment validation in Gradio Space discovery and origin/scheme enforcement for remote tool schemas. | **Embargoed (Vendor Triage)** |
| [`CVD-2026-APIFY-MCP-001`](https://ccsimplyspolit.github.io/advisories/CVD-2026-APIFY-MCP-001.html) | `apify/apify-mcp-server` | `CWE-200 / CWE-290` | Sensitive header redaction in telemetry trace identifiers and client tracking classification rules. | **Embargoed (Vendor Triage)** |
| [`CVD-2026-ARCADE-MCP-001`](https://ccsimplyspolit.github.io/advisories/CVD-2026-ARCADE-MCP-001.html) | `ArcadeAI/arcade-mcp` | `CWE-22 / CWE-426 / CWE-209` | Path containment for recursive dependency includes, reserved environment variable filtering, and error redaction. | **Embargoed (Vendor Triage)** |
| [`CVD-2026-MONGODB-MCP-001`](https://ccsimplyspolit.github.io/advisories/CVD-2026-MONGODB-MCP-001.html) | `mongodb-js/mongodb-mcp-server` | `CWE-863 / CWE-20` | One-way security override enforcement for delimiter guards and numeric bounds checking in request overrides. | **Embargoed (Vendor Triage)** |
| `CVD-2026-OMARCHY-001` | `omacom/omarchy` | `CWE-78 / CWE-20` | URI host string escaping in network captive-portal helpers and path validation in system scripts. | **Embargoed (Vendor Triage)** |
| [`CVD-2026-FAST-AGENT-001`](https://ccsimplyspolit.github.io/advisories/CVD-2026-FAST-AGENT-001.html) | `evalstate/fast-agent` | `CWE-22 / CWE-200` | Scheme allowlisting and local/UNC file path restriction in tool output resource handlers. | **Embargoed (Vendor Triage)** |
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
