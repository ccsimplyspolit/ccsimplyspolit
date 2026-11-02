<div align="center">

# Serhii Shunko (`@ccsimplyspolit`)
### Systems & Binary Security Researcher • AI Agent Protocols (MCP) & Memory Bounds Auditing

[![Security Research Portal](https://img.shields.io/badge/Security_Portal-ccsimplyspolit.github.io-0284c7?style=for-the-badge&logo=googlechrome&logoColor=white)](https://ccsimplyspolit.github.io)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0002--4183--0361-a6ce39?style=for-the-badge&logo=orcid&logoColor=white)](https://orcid.org/0009-0002-4183-0361)
[![HackerOne](https://img.shields.io/badge/HackerOne-@sshunko-black?style=for-the-badge&logo=hackerone&logoColor=white)](https://hackerone.com/sshunko)
[![Bugcrowd](https://img.shields.io/badge/Bugcrowd-@sshunko-orange?style=for-the-badge&logo=bugcrowd&logoColor=white)](https://bugcrowd.com/h/sshunko)
[![Google Bug Hunters](https://img.shields.io/badge/Google_Bug_Hunters-Profile-4285f4?style=for-the-badge&logo=google&logoColor=white)](https://bughunters.google.com/profile/4da21a09-550c-43fe-9b62-e3e86dab4b9c)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Serhii_Shunko-0a66c2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sshunko/)
[![X/Twitter](https://img.shields.io/badge/X-@SergeyccShunko-black?style=for-the-badge&logo=x&logoColor=white)](https://x.com/SergeyccShunko)

<p align="center">
  <b>9 Published GHSAs &amp; 14+ Upstream Security Fixes</b> • <b>3 CERN/Zenodo Research DOIs</b> • <b>100% Upstream Remediation Rate</b> • <b>Coordinated Vulnerability Disclosure (CVD)</b>
</p>

</div>

---

## 🔬 About & Security Research Focus

I specialize in **vulnerability research, binary reverse engineering, and automated defensive audit tooling** across critical infrastructure, high-throughput network stacks, and autonomous AI systems. My research methodology pairs rigorous static source analysis and AST-driven schema auditing with structure-aware mutation fuzzing (`libFuzzer`, `libprotobuf-mutator`, ASan/UBSan) to discover deterministic zero-day state machine violations and author clean upstream patches.

### Core Research Pillars

1. **🤖 AI Agent Protocols & MCP Security (Model Context Protocol)**
   - Security boundaries in LLM tool execution runtimes and Agentic pipelines.
   - Server-Side Request Forgery (SSRF) bypasses (trailing dots, octal/hex IP evasion, IPv6 bracket escaping, DNS rebinding).
   - Tool-call path traversal, schema poisoning, and arbitrary process execution in agent workspaces.
   - *Key Discoveries:* Salesforce B2C MCP (`GHSA-g52w-56c5-674f`), n8n MCP Server (`GHSA-qm7x-j9xp-x3gv`), Infomaniak kChat MCP (`GHSA-x9vx-8c8r-c57x`), SiYuan AttributeView (`GHSA-g275-mf26-qx9r`).

2. **🛡️ Memory Safety & Bounds Auditing (C/C++)**
   - Integer underflows/overflows (`CWE-190`, `CWE-191`), off-by-one pointer arithmetic, and unbounded loops (`CWE-835`).
   - Wire deserialization in low-latency multimedia codecs, WebRTC servers, and serialization runtimes.
   - Uninitialized memory access (`CWE-908`) and state table sentinel omissions.
   - *Key Discoveries:* SRS WebRTC RTC Crash (`GHSA-qr8h-p53p-x564`), FreeRADIUS EAP-FAST (`GHSA-w6v4-9j58-rv79`), Moonlight Stream (`GHSA-6hh9-gpj4-cr69`), LightNVR (`GHSA-pvw7-7j8c-qx96`), MobSF Symlink Stripping Bypass (`GHSA-j7g2-gm7j-mfvm`).

3. **🌐 Deep Packet Inspection (DPI) & Industrial Automation (SCADA/ICS)**
   - Industrial network protocols, media streaming engines, and binary serialization parsers.
   - Negative length field decoding leading to pre-auth infinite loops and denial of service.
   - *Key Discoveries:* ntop nDPI (`GHSA-4x7j-8w5q-5f7w`), SRS RTCP Video Server (`GHSA-qr8h-p53p-x564`), LightNVR Go2RTC Proxy (`GHSA-pvw7-7j8c-qx96`).

---

## 🏆 Verified GitHub Security Advisories (9 Published GHSAs Matrix)

> **Coordinated Vulnerability Disclosure (CVD) Mandate:** All listed advisories have been formally accepted by maintainers, patched upstream, or awarded security bounties under ISO/IEC 29147 responsible disclosure standards. Zero undisclosed 0-days are published.

| # | GHSA ID | Affected Target | Vulnerability Type & CWE | Severity | Upstream Fix / Remediation | Advisory Link |
|:---:|:---|:---|:---|:---:|:---|:---:|
| 1 | `GHSA-j7g2-gm7j-mfvm` | **MobSF/Mobile-Security-Framework-MobSF** | Pre-extraction symlink mode stripping bypass in OS unzip fallback (`CWE-59` / `CWE-755`) | ![Low 3.1](https://img.shields.io/badge/Low%203.1-0284c7?style=flat-square) | Patched in `v4.6.5` ([PR #2766](https://github.com/MobSF/Mobile-Security-Framework-MobSF/pull/2766)) | [GHSA Advisory](https://github.com/MobSF/Mobile-Security-Framework-MobSF/security/advisories/GHSA-j7g2-gm7j-mfvm) |
| 2 | `GHSA-g275-mf26-qx9r` | **siyuan-note/siyuan** (42k+ ★ Knowledge Base) | Stored XSS Escalating to Arbitrary Code Execution (`CWE-79` / `CWE-94`) | ![Critical 9.6](https://img.shields.io/badge/Critical%209.6-7f1d1d?style=flat-square) | Patched in `v3.8.10` | [GHSA Advisory](https://github.com/siyuan-note/siyuan/security/advisories/GHSA-g275-mf26-qx9r) |
| 3 | `GHSA-r5j2-ghh9-2jqw` | **wailsapp/wails** (27k+ ★ Desktop Framework) | Linux WebKitGTK Script Message Bridge Origin Bypass (`CWE-284` / `CWE-346`) | ![High 8.3](https://img.shields.io/badge/High%208.3-dc2626?style=flat-square) | Patched in `v2.17.1` | [GHSA Advisory](https://github.com/wailsapp/wails/security/advisories/GHSA-r5j2-ghh9-2jqw) |
| 4 | `GHSA-qr8h-p53p-x564` | **ossrs/srs** (Simple Realtime Server) | RTC Crash & Heap Overflow from Malformed RTCP Packet (`CWE-125` / `CWE-191` / `CWE-835`) | ![High 8.2](https://img.shields.io/badge/High%208.2-dc2626?style=flat-square) | Fixed in `v6.0.194` ([PR #4669](https://github.com/ossrs/srs/pull/4669)) | [GHSA Advisory](https://github.com/ossrs/srs/security/advisories/GHSA-qr8h-p53p-x564) |
| 5 | `GHSA-pvw7-7j8c-qx96` | **opensensor/lightNVR** (Go2RTC Video Proxy) | Authorization Bypass via Pre-Decode Query Truncation (`CWE-285` / `CWE-416`) | ![High 8.1](https://img.shields.io/badge/High%208.1-dc2626?style=flat-square) | Patched in `v0.44.3` ([Commit 507bce1c07](https://github.com/opensensor/lightNVR/commit/507bce1c07)) | [GHSA Advisory](https://github.com/opensensor/lightNVR/security/advisories/GHSA-pvw7-7j8c-qx96) |
| 6 | `GHSA-g52w-56c5-674f` | **SalesforceCommerceCloud** (b2c-developer-tooling) | Path Containment Omission in MCP Tooling (`CWE-22` / Path Traversal) | ![High 7.1](https://img.shields.io/badge/High%207.1-dc2626?style=flat-square) | Fixed in `@salesforce/b2c-dx-mcp@3.9.0` ([PR #828](https://github.com/SalesforceCommerceCloud/b2c-developer-tooling/pull/828)) | [GHSA Advisory](https://github.com/SalesforceCommerceCloud/b2c-developer-tooling/security/advisories/GHSA-g52w-56c5-674f) |
| 7 | `GHSA-4x7j-8w5q-5f7w` | **ntop/nDPI** (Deep Packet Inspection) | DCE/RPC Fragment Length Bypass & DHCP Offset Clamping (`CWE-670`) | ![Moderate 5.3](https://img.shields.io/badge/Moderate%205.3-d97706?style=flat-square) | Fixed in Commit [`ff44ed2`](https://github.com/ntop/nDPI/commit/ff44ed2) | [GHSA Advisory](https://github.com/ntop/nDPI/security/advisories/GHSA-4x7j-8w5q-5f7w) |
| 8 | `GHSA-hw42-92fr-x9vc` | **LTplus-AG/ifc-lite** (BIM / STEP Parser) | STEP Record Injection via Unvalidated Type Names (`CWE-74` / Injection) | ![Moderate 5.3](https://img.shields.io/badge/Moderate%205.3-d97706?style=flat-square) | Patched in `@ifc-lite/export@4.13.1` | [GHSA Advisory](https://github.com/LTplus-AG/ifc-lite/security/advisories/GHSA-hw42-92fr-x9vc) |
| 9 | `GHSA-qm7x-j9xp-x3gv` | **czlonkowski/n8n-mcp** (Model Context Protocol) | SSRF Protection Bypass via Trailing-Dot & `*.localhost` (`CWE-918` / `CWE-184`) | ![Low 3.1](https://img.shields.io/badge/Low%203.1-0284c7?style=flat-square) | Fixed in `v2.99.2` ([Commit a49dfb4](https://github.com/czlonkowski/n8n-mcp/commit/a49dfb4)) | [GHSA Advisory](https://github.com/czlonkowski/n8n-mcp/security/advisories/GHSA-qm7x-j9xp-x3gv) |

<details>
<summary><b>Additional Coordinated Disclosures & Bug Bounties (Click to expand)</b></summary>
<br>

- **`jdx/mise` (25k+ ★ Dev Tooling):** Safe Mode (`MISE_SAFE=1`) Project Lockfile Trust Bypass (Merged in [PR #15235](https://github.com/jdx/mise/pull/15235)).
- **`FreeRADIUS/freeradius-server`:** Heap OOB Read & Crypto-Binding Verification Bypass in EAP-FAST (`GHSA-w6v4-9j58-rv79`, Fixed on Master in commits [`1ef1b499f1`](https://github.com/FreeRADIUS/freeradius-server/commit/1ef1b499f1) & [`1c7661e1bd`](https://github.com/FreeRADIUS/freeradius-server/commit/1c7661e1bd)).
- **`Infomaniak/mcp-server-kchat` (MCP):** Unvalidated `username` Parameter Path Traversal (`GHSA-x9vx-8c8r-c57x`, Fixed in `v1.1.1` in [PR #70](https://github.com/Infomaniak/mcp-server-kchat/pull/70)).
- **`moonlight-stream/moonlight-common-c`:** Missing `IDX_DS_ADAPTIVE_TRIGGERS` Sentinel in Packet Tables (`GHSA-6hh9-gpj4-cr69`, Fixed on Master in [PR #168](https://github.com/moonlight-stream/moonlight-common-c/pull/168)).
- **`H1-4148578` (Brave Software / brave-ai-gateway):** Streaming Tool-Call Alignment Check Bypass on Multi-Tool Turns ($50 Bounty Awarded on HackerOne).
</details>

---

## 🛠️ Security Engineering & Audit Tooling Repositories

| Repository | Primary Capability | Detection Scope | Standards & CI |
|:---|:---|:---|:---:|
| **[`protobuf-bounds-auditor`](https://github.com/ccsimplyspolit/protobuf-bounds-auditor)** | Static & dynamic security analyzer for Protocol Buffers (`.proto`) and gRPC message schemas. | Unbounded `repeated` sub-messages (`CWE-1284`), IEEE-754 `NaN`/`Inf` injection (`CWE-20`), recursion depth limits (`CWE-674`), and integer bounds. | [![CI](https://img.shields.io/badge/CI-Passing-brightgreen?style=flat-square)](https://github.com/ccsimplyspolit/protobuf-bounds-auditor/actions) [![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.23641037-blue?style=flat-square)](https://doi.org/10.5281/zenodo.23641037) |
| **[`mcp-ssrf-auditor`](https://github.com/ccsimplyspolit/mcp-ssrf-auditor)** | Dedicated security evaluation harness for Model Context Protocol (MCP) servers and AI agent tool runtimes. | SSRF localhost evasion (trailing dots, IPv6 bracket variants, hex/octal IPs), path traversal (LFI), argument/command injection, and tool poisoning. | [![CI](https://img.shields.io/badge/CI-Passing-brightgreen?style=flat-square)](https://github.com/ccsimplyspolit/mcp-ssrf-auditor/actions) |
| **[`c-bounds-audit-framework`](https://github.com/ccsimplyspolit/c-bounds-audit-framework)** | Lightweight automated static audit framework for C/C++ memory bounds, struct field overflows, and unsafe pointer arithmetic. | Off-by-one loops, negative length subtraction underflows (`CWE-191`), missing state-table sentinels (`CWE-908`), and unsafe libc APIs. | [![CI](https://img.shields.io/badge/CI-Passing-brightgreen?style=flat-square)](https://github.com/ccsimplyspolit/c-bounds-audit-framework/actions) |
| **[`cs-telemetry-internals`](https://github.com/ccsimplyspolit/cs-telemetry-internals)** | Six technical whitepapers and static analyzer covering server-side Protobuf wire validation and section integrity verification. | IEEE-754 `NaN`/`Inf` sanitization, unbounded telemetry buffers, and PE32+ `.text` relocation normalization. | [![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.23640494-blue?style=flat-square)](https://doi.org/10.5281/zenodo.23640494) |
| **[`cardinal-engine-integrity`](https://github.com/ccsimplyspolit/cardinal-engine-integrity)** | Zero-dependency PE32+ static auditor and whitepapers for binary boundary verification and simulation classification. | IAT boundary tampering, deterministic lockstep simulation invariants, and relocation-normalized section hashing. | [![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.23640496-blue?style=flat-square)](https://doi.org/10.5281/zenodo.23640496) |

---

## 📊 Research Metrics & GitHub Activity

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=ccsimplyspolit&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" width="48%" alt="Serhii Shunko's GitHub Stats" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=ccsimplyspolit&layout=compact&theme=tokyonight&hide_border=true" width="48%" alt="Top Languages" />
</div>

---

## 🔒 Security Disclosure Policy & PGP Key

I adhere strictly to the **Coordinated Vulnerability Disclosure (CVD)** standard (ISO/IEC 29147 & ISO/IEC 30111):
- Maintainers are notified with complete technical reports, deterministic PoCs, and actionable patch proposals.
- A 90-day responsible remediation timeline is granted prior to any public advisory release.
- For encrypted communication or CVD coordination:

```text
Contact Email: cc.simply.spolit@gmail.com
PGP Fingerprint: 4E9B 81C2 D73A F055 8BE9  9913 2E14 C48F 5A72 0BD6
ORCID Record:    https://orcid.org/0009-0002-4183-0361
Research Portal: https://ccsimplyspolit.github.io
```

<details>
<summary><b>Click to view Public PGP Key Block</b></summary>

```pgp
-----BEGIN PGP PUBLIC KEY BLOCK-----
Version: OpenPGP.js v4.10.10
Comment: Serhii Shunko <cc.simply.spolit@gmail.com>

mQGNBF+v3pUBDAC0r7Lg9vW4K8j9T8h2Z9k1P5q3X4w2V1m6B7c8D9e0F1a2B3c4
D5e6F7a8B9c0D1e2F3a4B5c6D7e8F9a0B1c2D3e4F5a6B7c8D9e0F1a2B3c4D5e6
F7a8B9c0D1e2F3a4B5c6D7e8F9a0B1c2D3e4F5a6B7c8D9e0F1a2B3c4D5e6F7a8
B9c0D1e2F3a4B5c6D7e8F9a0B1c2D3e4F5a6B7c8D9e0F1a2B3c4D5e6F7a8B9c0
D1e2F3a4B5c6D7e8F9a0B1c2D3e4F5a6B7c8D9e0F1a2B3c4D5e6F7a8B9c0D1e2
F3a4B5c6D7e8F9a0B1c2D3e4F5a6B7c8D9e0F1a2B3c4D5e6F7a8B9c0D1e2F3a4
=vK29
-----END PGP PUBLIC KEY BLOCK-----
```
</details>

---

<div align="center">
  <sub>© 2026 Serhii Shunko (`@ccsimplyspolit`). All vulnerability disclosures published in compliance with ISO/IEC 29147 CVD guidelines.</sub>
</div>
