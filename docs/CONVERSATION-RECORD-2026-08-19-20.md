# Project conversation record — 19–20 August 2026

> This document records the visible, substantive conversation for the ITOL Change Assistant project. It excludes hidden system instructions, tool output, and private reasoning. The original user-supplied project brief is preserved verbatim in [PROJECT-BRIEF.md](PROJECT-BRIEF.md).

## Initial request

### User

> Plan this out first, spawn relevant subagents. Worth noting that PDF files etc is living on Sharepoint/Onedrive.

### Assistant

Planned the project as a discovery-first programme. The resulting architecture keeps PipesHub as the permission-aware context, search, citation, and agent layer, while an ITOL-owned Change Service owns manifests, approvals, execution gates, policies, and audit records.

The plan established these major stages:

1. Establish programme boundaries, owners, environments, access constraints, and pilot success criteria.
2. Inspect and pin PipesHub; document extension points, auth, graph, approval/HITL, connector, MCP, and deployment choices.
3. Prove a local read-only PipesHub deployment with a test Obsidian vault and source citations.
4. Build ASK and INVESTIGATE flows, entity registry, dependency model, and evidence-led discovery.
5. Add read-only WordPress Recruit, HubSpot, and SharePoint/OneDrive adapters; deliver the impact-report milestone.
6. Build the standalone ITOL Change Service with Postgres-backed manifests, audit events, state machine, policies, and human tasks.
7. Integrate Monday as the manifest-bound approval control plane; implement fail-closed safety tests.
8. Prove one reversible, low-risk WordPress staging write.
9. Run a narrow production pilot and expand only after safety and accuracy targets are achieved.

## Architecture conclusions

### Assistant

- PipesHub is the employee-facing discovery/context layer, not the change-control system of record.
- The Change Service must hold canonical, typed, immutable manifests; approval binds to `change_id + manifest_version + manifest_hash`.
- Operational applications retain live truth; Obsidian is governed organisational truth; the Change Manifest is change truth.
- The assistant must separate ASK, INVESTIGATE, and SUBMIT. Investigation never authorises a write.
- LLMs interpret intent and select only typed, allow-listed actions. Deterministic adapters perform any production write.
- All failures in approval, hash integrity, current-state checks, permissions, connector health, or risk assessment fail closed.
- Pre-flight and validation use live APIs, never an index alone.
- Cross-system execution uses idempotent action records, independent read-back/validation, and explicit compensation or human recovery.

## SharePoint / OneDrive direction

### Assistant

SharePoint Online and OneDrive for Business are first-class federated operational document stores, not merely locations for PDFs.

Phase 1 is an ITOL-owned, read-only Microsoft 365/Graph connector or narrow MCP service. It provides constrained discovery operations only: document search, metadata, extraction, citations, live version checks, and optional version history.

The initial scope should be named SharePoint sites/libraries. Individual OneDrives remain excluded unless explicitly approved because of privacy and ownership risk.

Each document discovery preserves tenant/site/drive/item identity, URL/path, eTag/version, modification time, source freshness, parser version, citation anchor, and evidence hash. A later write would need live version/eTag confirmation before action and post-write file validation. PDF rewriting is not a generic action: where no approved editable source exists, create a human task instead.

## Monday.com delivery-board request

### User

> In the AI Integration & RAG - Delivery Board I've created a group called ITOL Change Assistant.
>
> Could you please create all the plan tasks there, assign them to myself and set realisting due date. Each task should have a comment with a briefing (or what needs to be done). Don't need to assign anyone else to these tasks.
>
> Please do that now

### Assistant

Created the following tasks in the **ITOL Change Assistant** group, assigned only to Herman, with detailed initial briefing comments:

| # | Task | Due date |
|---:|---|---|
| 0 | Maintain project blueprint, ADRs & delivery controls | 25 Sep 2026 |
| 1 | Establish scope, access & pilot success criteria | 4 Sep 2026 |
| 2 | Complete PipesHub architecture & extension discovery | 25 Sep 2026 |
| 3 | Prove local read-only PipesHub & Obsidian foundation | 16 Oct 2026 |
| 4 | Build ASK/INVESTIGATE assistant & entity registry | 6 Nov 2026 |
| 5 | Deliver read-only cross-system impact-report milestone | 4 Dec 2026 |
| 6 | Build ITOL Change Service governance foundation | 15 Jan 2027 |
| 7 | Integrate Monday approval control plane & safety gate | 5 Feb 2027 |
| 8 | Prove one controlled WordPress staging write | 5 Mar 2027 |
| 9 | Run constrained production pilot & readiness review | 26 Mar 2027 |

The tasks were marked **Working on it**, with **RAG health: Amber** and **Approval required: Required**, matching the board’s governance model.

## Ongoing board maintenance

### User

> As we work on this project even on future sessions within this project, please make to contininiously update that specific group. You can update tasks, edit then, add new one, create sub tasks etc etc. Please just make sure to continiously update it going forward for this project.

### Assistant

Confirmed that the **ITOL Change Assistant** group is the live delivery record. Future work will keep tasks, due dates, progress, briefs, subitems, blockers, and new work up to date.

## Blueprint request

### User

> Please show me the full detailed plan

### Assistant

Provided the detailed nine-stage delivery plan covering scope/access, PipesHub discovery, local knowledge foundation, read-only assistant and entity registry, cross-system impact reporting, Change Service governance, Monday approval controls, staging write proof, and constrained production pilot.

### User

> Where is the blueprint etc?

### Assistant

Created the board item **0. Maintain project blueprint, ADRs & delivery controls** and attached a living Monday document titled **ITOL Change Assistant — Project Blueprint**. It contains:

- purpose and target operating model;
- federated-truth model;
- ASK / INVESTIGATE / SUBMIT workflow;
- governance and safety controls;
- change lifecycle;
- core domain records;
- initial connector posture;
- SharePoint/OneDrive treatment;
- pilot definition;
- delivery sequence;
- architecture-decision record list; and
- safe-expansion criteria.

The blueprint is maintained alongside the delivery tasks.

## Publication request

### User

> Please send all chat that we had here, as well as the pasted text to the github repo here https://github.com/thefilthycasual/itolchange

### Assistant

Verified that the requested repository is public and requested confirmation before publishing internal project materials.

### User

> yes confirmed

### Assistant

Publishing the original pasted project brief and this visible conversation record to the confirmed public repository.