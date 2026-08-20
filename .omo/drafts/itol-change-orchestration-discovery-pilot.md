---
slug: itol-change-orchestration-discovery-pilot
status: reviewed-approved-awaiting-start
intent: unclear
pending-action: write .omo/plans/itol-change-orchestration-discovery-pilot.md
approach: Build a contract-first, read-only discovery pilot for one provisional ITOL Recruit Project Management salary-claim scenario; validate discovery against a governed ground-truth corpus before any approval-board creation or external write.
---

# Draft: itol-change-orchestration-discovery-pilot

## Components (topology ledger)
<!-- Lock the SHAPE before depth. One row per top-level component that can succeed or fail independently. -->
| C1 | Repository architecture, ADRs, contracts, and a deterministic policy boundary | active | /Users/herman/Library/CloudStorage/OneDrive-ITonlinelearningLtd/General - Marketing/Obsidian Vaults/ITOL/Shared/Governance/AI Integration Roadmap.md:39-76; plan todos 2-4 |
| C2 | Pilot entity/evidence/ground-truth pack that is explicit about authority and unresolved identity | active | .../Shared/Product Knowledge/Product Source of Truth.md:1-54; .../Departments/Design & Email/Canva Inventory Register.md:110-118 |
| C3 | Read-only discovery adapters and safe retrieval boundary | active | .../AGENTS.md:60-82; .../Shared/Governance/Automation Policy.md:77-91 |
| C4 | Deterministic intake, match classification, and impact preview | active | Plan todos 12-14; .../AI Integration Roadmap.md:68-76 |
| C5 | Measurable quality, redacted audit evidence, and operational go/no-go controls | active | Plan todos 15-18; .../AI Integration Roadmap.md:320-331 |
| C6 | Monday Change Control design only; board provisioning and approval automation deferred | deferred | User approval: dedicated private Change Control board; .../Platforms/monday.com.md:1-50 |

## Open assumptions (announced defaults)
<!-- Intent is UNCLEAR: research resolves ambiguity, defaults are adopted (not asked), and each is surfaced in the plan's human TL;DR for veto. -->
| The ITOL vault is governance/pointer memory, not a global master database | Preserve the vault's stated federated boundaries and re-read operational sources | Yes |
| The pilot starts with one synthetic-or-approved salary scenario, not the £30k–£40k example as a live fact | No approved Project Management salary evidence was found; the inspected page is a working draft | Yes |
| Salary, outcome, and placement claims are High risk | Vault claim controls require verified evidence and routed approval | Yes |
| Entity identity remains provisional until PP019 / PMQ relationship is resolved | The Canva register records both names separately | Yes |
| Pilot retrieval is restricted to approved ITOL roots and excludes Autopilot, Archive, companion vaults, PII, and lead data | Root vault controls and Autopilot isolation boundary | Yes |
| The pilot uses a deterministic, narrow salary-change parser; no LLM receives vault or live-system content | A one-entity/fact pilot is safer and measurable without an unbounded model | Yes |
| Bun + strict TypeScript + Biome + Bun test is the initial runtime/toolchain | Empty repository; typed contracts and deterministic fixture tests are the smallest reversible baseline | Yes |
| Registry/graph are versioned YAML pointers for the pilot; durable runtime persistence is deferred | Avoid a production database before discovery quality is proven | Yes |
| A dedicated private Monday Change Control board is designed now but provisioned only after read-only pilot exit criteria pass | User approved dedicated-board direction; no pilot write is permitted | Yes |

## Findings (cited - path:lines)

- The vault assigns the vault to approved rules, reusable knowledge, decisions, and lessons; Monday, WordPress, HubSpot, and Canva retain live-system ownership: .../ITOL/AGENTS.md:60-69 and .../Shared/Governance/Company Sources of Truth.md:25-43.
- External writes require explicit approval and a separately recorded confirmation: .../Shared/Governance/Human Approval Policy.md:9-42.
- The automation pilot prohibits automatic publication, CRM writes, and assumes no connector is installed/authenticated/authorised merely because it is documented: .../Shared/Governance/Automation Policy.md:7-21, 77-114.
- Product values belong in the Product Source of Truth and publishable artefacts must cite a PST reference: .../Shared/Product Knowledge/Product Source of Truth.md:10-54.
- ITOL Recruit salary and outcome wording requires verified evidence and documented approval: .../Brands/ITOL Recruit/Brand Profile/Commercial Context and Claim Controls.md:11-18 and .../Brand Profile/Shop Programme Management.md:18-26.
- The ITOL Recruit sitemap is a placeholder and cannot seed completeness claims: .../Departments/Web/ITOL Recruit/Website Sitemap/ITOL Recruit Website Sitemap.md:1-24.
- The Canva inventory contains distinct PP019 Project Management and PMQ records: .../Departments/Design & Email/Canva Inventory Register.md:110-118.
- The PM Jobs landing page is an unapproved working draft and explicitly requires claim verification, technical testing, and named approvals: .../Departments/PPC/Google Ads/ITOL Recruit/Landing Pages/Google Ads/PM Jobs - ITOL Recruit (London and UK) - Landing Page Draft.md:1-6, 50-84.
- The current repository has no product source, documentation, or committed baseline; this plan creates the first implementation surface.

## Decisions (with rationale)

- Build a read-only discovery core rather than a portal, executor, or approval automation. This proves discovery quality before consequential capability exists.
- Treat retrieved vault/live text as evidence only. It never supplies executable instructions, credentials, or authority over deterministic policy.
- Make the live-pilot gate machine-checkable: a missing approved claim-evidence reference, unresolved target identity, unavailable adapter capability, or failed ground-truth threshold blocks the preview from claiming completeness.
- Design the dedicated Monday board as a future control-plane contract, not a pilot integration. The design includes immutable manifest/version/hash fields and links to existing departmental boards, but makes no Monday mutation.

## Scope IN

- A runnable internal, read-only discovery pilot core and CLI/API preview using fixture-backed and capability-gated live adapters.
- Schema-valid request, evidence, entity, dependency, match, risk, impact-preview, and future manifest contracts.
- Redacted technical audit records, quality metrics, runbooks, and a future private Monday Change Control board specification.

## Scope OUT (Must NOT have)

- No production, staging, Monday, WordPress, HubSpot, Canva, OneDrive, SharePoint, CRM, lead, email, form, Zapier, or database write.
- No AutoPilot retrieval or modification; no retrieval from companion vaults or Archive; no PII, raw lead, cookie, webhook, or credential collection/storage.
- No generic autonomous agent, broad RAG ingestion, public web portal, SSO integration, scheduler, proactive monitoring, approval webhook, board creation, or execution engine.
- No use of unapproved salary figures or assertion that all organisational references have been found.

## Open questions

- None block this plan. The live pilot remains mechanically blocked until the Product owner supplies approved salary-claim evidence and resolves the provisional PP019 identity mapping.

## Approval gate
status: approved-to-write-plan 2026-08-18
approval: User approved a dedicated private Monday Change Control board and explicitly authorised writing this discovery-pilot plan. This approval does not authorise implementation or any external write.

## Review receipts

- Metis review `ses_feacef6c1ffefZhvuF4QW6L5Qq`: CHANGES REQUIRED. Incorporated toolchain reconciliation; authority precedence; freshness and verification status; source-pointer rule; prompt-injection fixture; form/lead-handler URL denial; exact HubSpot category allow-list; Canva human-assisted-only clarification; dependency corrections; OS-level loopback test; realistic redaction; and unapproved-evidence release test.
- Momus first pass `ses_feac5abd6ffeutE2tb1KUI2npD`: APPROVE with a non-blocking conversational-brief reference observation.
- Independent Oracle first pass `ses_feac5ab92ffeoDThlBfZ7UdMvM`: CHANGES REQUIRED because the user architecture brief was unavailable to a downstream worker. Removed every such reference and made the affected todos self-contained.
- Momus fresh pass `ses_feac05852ffeEVtT4S0Htel3Ag`: APPROVE.
- Independent Oracle fresh pass `ses_feac057c9ffewcnxyJNQ6yytO3`: APPROVE.
- Momus final pass `ses_feabeb4feffepgxhcv2UUt9fmY`: APPROVE after final-verification-wave detail was added.
- Independent Oracle final pass `ses_feabeb50affe3FZQzjFyoD0PVq`: APPROVE; confirmed F1-F4 are agent-executable and preserve no-write, no-PII, safe-retrieval, and scoped-completeness constraints.
