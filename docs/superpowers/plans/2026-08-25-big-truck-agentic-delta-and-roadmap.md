# Big Truck Agentic Delta and Roadmap Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Write one evidence-disciplined Speckle-facing Big Truck Agentic Delta and one independently executable proof-gate Roadmap without changing Riff or implementing the POC.

**Architecture:** The Delta owns the durable argument, claim ledger, product boundaries, measured agentic hypothesis, and bounded protocol opportunities. The Roadmap owns execution order, reproducible runtime pins, gate-specific verification, risks, and stop/go rules; it references stable Delta claim IDs instead of repeating the argument.

**Tech Stack:** Markdown, Git, ripgrep, PowerShell or POSIX shell for Git commands, and Python standard-library one-liners for cross-platform document validation.

**Spec:** `docs/superpowers/specs/2026-08-24-speckle-riff-spike-document-design.md`

> **Post-execution review amendment (2026-08-25):** The delivered contracts must also bind the reviewed source version, whole-document canvas fingerprint, and live `before` state; carry one complete `RookActionBinding`; require Rook fingerprint capture and a narrow mutation-bound `gh_compare_and_set_value` operation; prevent replay with an atomically persisted tuple-keyed one-use permit; and avoid a self-referential package commit pin. The separately authorized README alignment remains a distinct commit. These corrections supersede narrower executor-field lists below where they conflict.

## Global Constraints

- Work from the `speckle-riff-spike` repository root.
- Read the complete specification before editing either target document.
- The original execution creates only `docs/big-truck-agentic-delta.md` and `ROADMAP.md`; approved post-execution contract corrections may amend this plan and its specification for consistency.
- Do not edit Riff, Chirp, Rook, upstream Speckle clones, or generated POC artifacts. README alignment is allowed only as the separately authorized small follow-up commit.
- Do not implement a harness, connector, emulator, fixture generator, sidecar writer, or POC action.
- Use only publicly inspectable sources and pinned repository revisions; never copy private schemas, credentials, licensed binaries, or proprietary examples.
- Every material Big Truck statement must use exactly one state: `observed_upstream`, `proven_locally`, `poc_hypothesis`, or `requires_speckle_validation`.
- A mutable branch is not a released specification. Cite repository, branch, full SHA, observation date, and exact source path.
- Source precedence is executable code/tests at the pinned SHA, then current handoff documents, then planning documents, then our interpretation.
- Keep contradictions visible. Do not reconcile incompatible upstream documents by guessing.
- The POC completion claim uses only released public Speckle capabilities and does not depend on Big Truck or Speckle collaboration.
- Gates 0–2 are the required POC. Gates 3–4 are independently stoppable post-POC research. Gate 5 is optional Speckle validation.
- Riff owns reasoning, review, and decision semantics; the spike owns durable capture, cryptographic binding, execution lineage, and verification artifacts.
- `review_complete` never means authorized. POC execution requires every node accepted and exactly one reviewed `payload.agentic_change_candidate`.
- Execution must copy `source_version`, `source_canvas_state_fingerprint`, `before`, and one complete reviewed `RookActionBinding`; static checks happen before permit creation, while Rook compares all live canvas/identity/value guards atomically with mutation. Static failure refuses; a live mismatch after invocation is a failed authorized attempt with no mutation.
- An atomically persisted permitted `PreflightResult` consumes one possible attempt. Replay, failure, or uncertainty after permit creation requires a new snapshot and review.
- A failed preflight produces no action and no `AgenticChangeRecord`. Failure after the authorized executor is invoked produces an immutable failed outcome record.
- Numeric verification uses the explicit reviewed unit and absolute tolerance with no implicit conversion.
- Karamba evidence and all agent reasoning remain advisory; human authorization is not structural approval or professional sign-off.
- Commands and document paths must work unchanged on Windows and macOS from the repository root.
- Stop after document verification and reviewer handoff. Do not begin POC implementation, push, or open a pull request.
- After human approval, commit this plan alone, record that commit as `PLAN_SHA`, and begin Task 1 from a clean worktree. The plan remains uncommitted while it is under review.

## File Responsibilities

| File | Responsibility |
| --- | --- |
| `docs/big-truck-agentic-delta.md` | Speckle-facing proposition, evidence ledger, observed Big Truck direction, agentic delta, ownership boundaries, lineage seam, measurement rules, protocol opportunities, and permitted/prohibited claims |
| `ROADMAP.md` | Current status, reproducible runtime ledger, Gates 0–5, deliverables, verification matrix, risks, stop/go rules, and promotion boundary into Riff |

## Stable Cross-Document Interfaces

The Delta defines claim IDs using these prefixes:

```text
BT-OBS-###       observed upstream Big Truck behavior
POC-PROOF-###    locally demonstrated POC behavior
BT-HYP-###       measurable hypothesis
BT-VALIDATE-###  claim requiring Speckle validation
PROTO-###        bounded protocol opportunity
```

The Roadmap may reference those IDs but may not redefine their argument. Claim IDs never change meaning after publication; a superseded claim receives a status note rather than being silently rewritten.

The Delta and Roadmap group lifecycle terms by namespace:

```text
Execution checkpoints: preflight_refused | execution_attempted
Record outcomes:       verified | failed
Gate statuses:         not_started | in_progress | blocked | complete | optional
```

---

### Task 1: Write the Speckle-Facing Big Truck Agentic Delta

**Files:**
- Create: `docs/big-truck-agentic-delta.md`
- Read: `docs/superpowers/specs/2026-08-24-speckle-riff-spike-document-design.md`
- Read: `README.md`
- Inspect only: `speckle-sharp-sdk-big-truck/**`
- Inspect only: `speckle-sharp-connectors-big-truck/**`
- Inspect only: `speckle-server/**`
- Inspect only: `specklepy/**`
- Inspect only: `speckle-docs/**`

**Interfaces:**
- Consumes: the approved design specification and pinned upstream repositories.
- Produces: stable claim IDs and capability arguments that `ROADMAP.md` references.

- [ ] **Step 1: Verify the design and upstream evidence baseline before writing**

Run:

```text
git status --short --branch
git show --stat --oneline 7726b57b1e6f116ef8e41518411b7dfc9498e24a
git -C speckle-sharp-sdk-big-truck rev-parse HEAD
git -C speckle-sharp-connectors-big-truck rev-parse HEAD
git -C speckle-server rev-parse HEAD
git -C specklepy rev-parse HEAD
git -C speckle-docs rev-parse HEAD
```

Expected:

```text
HEAD is the approved plan commit recorded as PLAN_SHA and the worktree is clean.
The design commit contains only the specification.
The upstream SHAs match the specification, or the writer stops and records that the evidence baseline must be re-reviewed before authoring claims.
```

Required pinned values:

```text
speckle-sharp-sdk big-truck:        f87d39cff9f54aff6c30b634780c834ba070ff4e
speckle-sharp-connectors big-truck: 0313a89878d5d91c7b69e0492da4dd7b6c76b51d
speckle-server main:                51d43b91c4681a75bff8b285da7f443a4599da67
specklepy main:                     5481458ecbae39f357f247deb33cb4976000e966
speckle-docs main:                  5d88e384b62688a9b0443ad72b13069b7b16e639
```

- [ ] **Step 2: Create the complete Delta document shell**

Create `docs/big-truck-agentic-delta.md` with these exact top-level sections:

```markdown
# Big Truck Agentic Delta

> **Status:** Independent integration research observed at pinned upstream revisions on 2026-08-24. This is not a Speckle specification, compatibility claim, or product commitment.

## Executive Proposition
## Independent Project Disclaimer
## The Demonstration
## What the Released-Speckle POC Proves
## Big Truck Evidence Ledger
## Big Truck's Potential Agentic Delta
## Canonical Evidence and Action Lineage
## Identity Guarantees and Limits
## Responsibility and Authority Boundaries
## Temporary-to-Native Replacement Map
## Measurement Strategy
## Protocol Opportunities
## Permitted and Prohibited Claims
## Questions for Speckle
## Source Notes
```

- [ ] **Step 3: Write the executive proposition**

Use this executive proposition verbatim before expanding it:

```markdown
Speckle supplies durable, versioned project evidence. Riff supplies inspectable reasoning and consequential human authority. This spike tests whether they can be joined into a verified, auditable agent-action loop without making Riff a geometry store or treating human review as professional engineering approval.

The proposition is not that Big Truck supplies reasoning. Big Truck may make version-scoped identity, properties, topology, and selectively readable evidence substantially more useful to agents. Chirp interprets evidence, Riff exposes and records reasoning and authority, and the external agent acts only through a bounded executor after authorization.
```

- [ ] **Step 4: Write the independent-project disclaimer**

Under `## Independent Project Disclaimer`, state:

```markdown
This is an independent, unofficial integration research project. It is not authored, endorsed, or certified by Speckle. Observations describe pinned public source revisions and may not represent the released or eventual Big Truck product. No private specification, credential, licensed binary, staging detail, or proprietary example is reproduced here.
```

- [ ] **Step 5: Write the responsibility boundary**

Place this concise boundary in `## Executive Proposition` after the proposition:

```text
Speckle / Big Truck  → project evidence and version plane
Karamba              → preliminary deterministic analysis
Chirp                → structured interpretation and proposal
Riff                 → inspectable reasoning and human decision semantics
External main agent  → orchestration
Rook                 → one allowlisted Grasshopper action
Spike                → durable capture, lineage, verification, and comparison
```

- [ ] **Step 6: Write the POC lifecycle narrative**

Include this complete lifecycle:

```text
Speckle version A
→ bounded evidence and preliminary Karamba results
→ Chirp interpretation and one exact agentic_change_candidate
→ Riff presentation and per-node human review
→ all nodes accepted and exactly one authorizing candidate
→ raw Review Matrix response written, hashed, read back, and verified
→ external agent coordinates one allowlisted Rook action
→ Speckle version B is published
→ B is independently re-read and verified
→ one immutable AgenticChangeRecord binds the lineage
```

- [ ] **Step 7: Write the authorization and failure semantics**

State all of the following explicitly:

```text
- A failed authorization or sidecar preflight performs no action and creates no AgenticChangeRecord.
- Failure after the authorized executor is invoked creates outcome: failed.
- A failed verification can retain result_version B when B was published.
- Review Matrix review_complete is necessary but insufficient; every node must be accepted.
- Exactly one node may contain payload.agentic_change_candidate.
- Riff annotations, including change_candidate, are advisory and non-executable.
- JSON sidecars are POC packaging, not the proposed permanent Big Truck representation.
```

- [ ] **Step 8: Write the lineage seam**

Describe `AgenticChangeRecord` by linking to the specification rather than copying the entire field tree. Copy only its semantic layers:

```text
source evidence
→ exact authorization artifact and action candidate
→ attempted action
→ result version when published
→ deterministic verification
→ verified or failed outcome
```

- [ ] **Step 9: Locate the primary Big Truck evidence**

Run these source-location commands and use their exact resulting paths in citations:

```text
rg -n "12|parquet|geometry|eav|envelope|schemaVersion|artifacts" speckle-sharp-sdk-big-truck/Speckle-4.0-Plan.md speckle-sharp-sdk-big-truck/notes speckle-sharp-sdk-big-truck/plans
rg -n "application_id|object_index|relation|DISPLAY|SOLID|SUBELEMENT|HAS_MATERIAL|ON_LEVEL" speckle-sharp-sdk-big-truck
rg -n "UseArtifacts|PreferArtefacts|SendArtefact|ReceiveArtefact|ExploreComponent" speckle-sharp-connectors-big-truck
rg -n "api/v2/projects|artifacts|presigned" speckle-sharp-sdk-big-truck speckle-server
rg -n "speckle-bundle-spec|schema_version" speckle-sharp-sdk-big-truck speckle-sharp-connectors-big-truck
```

- [ ] **Step 10: Create the evidence-state definitions and ledger shell**

Define all four evidence states before the ledger:

```text
observed_upstream             directly supported by a pinned public upstream source
proven_locally                supported by a retained local artifact and repeatable verification
poc_hypothesis                a claim with a named local experiment that has not yet passed
requires_speckle_validation   a claim that cannot be resolved from public local evidence
```

Create a ledger with this exact schema:

```markdown
| Claim ID | Evidence state | Claim or observation | Repository / branch / SHA | Source | Contradiction or limitation |
| --- | --- | --- | --- | --- | --- |
```

- [ ] **Step 11: Ground the bundle, namespace, identity, and geometry observations**

Add:

```text
BT-OBS-001  The pinned SDK handoff describes a 12-file Zstd Parquet bundle split across geometry, EAV, and envelope tables.
BT-OBS-002  The pinned model separates object, geometry, and node namespaces and uses typed relations to connect them.
BT-OBS-003  application_id is an addressing key, but cross-version continuity remains producer-dependent.
BT-OBS-004  The pinned bundle stores geometry separately from EAV and envelope/topology artifacts.
```

- [ ] **Step 12: Ground the endpoint, branch-maturity, and reproducibility observations**

Add:

```text
BT-OBS-005  The handoff describes a version-artifacts endpoint, while the pinned public server main does not independently prove that endpoint is available.
BT-OBS-006  The public Big Truck branches contain evolving artifact send/receive or exploration work and internally superseded planning material.
BT-OBS-007  Reproducible local generation may remain blocked by unavailable generated speckle-bundle-spec dependencies and required toolchain versions.
```

- [ ] **Step 13: Add the POC proof, agentic hypothesis, and validation claims**

Add:

```text
POC-PROOF-001  The released-Speckle A-to-B authority loop is a poc_hypothesis until Gate 2 retains passing evidence; only then may its state become proven_locally.
BT-HYP-001  Separate and selective property/topology artifacts can enable geometry-independent evidence questions and reduce transferred bytes, geometry materialization, and normalized agent context for equivalent answers.
BT-VALIDATE-001  Native compatibility with Speckle's unreleased service requires Speckle validation.
```

Apply states explicitly: every `BT-OBS-*` row is `observed_upstream`; `POC-PROOF-001` begins as `poc_hypothesis`; `BT-HYP-001` is `poc_hypothesis`; and `BT-VALIDATE-001` is `requires_speckle_validation`. State that no POC behavior is `proven_locally` before Gate 2 passes.

Use direct GitHub permalinks containing the full commit SHA when the cited upstream file is public. Never cite a search-result page or mutable `main` URL as permanent evidence.

- [ ] **Step 14: Write the capability-delta table**

Use one capability table:

```markdown
| Capability | Released-path baseline | Observed Big Truck direction | Agentic consequence | Current evidence state | Proof required |
| --- | --- | --- | --- | --- | --- |
```

Cover only:

```text
version-scoped evidence
object addressing and producer identity
typed properties
topology and relationships
geometry-independent reads
columnar and bounded consumption
artifact reuse between agents
cross-version comparison when identity is stable
```

Do not say that current Speckle is not machine-readable. State that the hypothesized delta is purpose-separated, bounded, columnar, version-scoped consumption with explicit topology—not machine readability appearing from nothing.

- [ ] **Step 15: Write the correctness-first measurement strategy**

Define the comparison as correctness first, then this transparent scorecard:

```text
facts resolved correctly
identity and relationships preserved
bytes transferred or read
objects and geometry materialized
elapsed retrieval time
normalized evidence size
model-input tokens
```

State that the real civic canopy is primary. One or two deterministic scale variants are permitted only if the real model is too small to reveal an interpretable difference. Do not create a composite score or extrapolate production performance.

- [ ] **Step 16: Write the temporary-to-native replacement map**

The map must distinguish:

```text
Temporary released path     Current Speckle object API or SDK plus released Grasshopper connector sanity check
Durable spike contract      Evidence references, authorization policy, sidecar digest, AgenticChangeRecord, deterministic verification
Potential native path       Big Truck artifact discovery and bounded evidence consumption after validation
Disposable work             Transport-specific adapters and any local protocol emulator
```

- [ ] **Step 17: Write Protocol Opportunity PROTO-001**

Use this exact entry schema:

```text
opportunity_id
problem_observed
agentic_benefit
upstream_evidence
current_limitation
candidate_protocol_capability
compatibility_concern
validation_needed
status
```

Use the schema to write only the identity-continuity entry:

```text
PROTO-001  identity continuity metadata
```

Phrase it as a question for Speckle, not a requirement.

- [ ] **Step 18: Write Protocol Opportunities PROTO-002 and PROTO-003**

Use the same schema to write:

```text
PROTO-002  grounded derived-evidence references
PROTO-003  artifact capability discovery
```

Phrase each as a question for Speckle, not a requirement. Include an explicit statement that an opportunity is retired if evidence shows Big Truck already solves it or the POC does not need it.

- [ ] **Step 19: Write the permitted and prohibited claim guardrails**

The prohibited-claims subsection must include:

```text
Big Truck is a final or stable public specification.
Big Truck universally guarantees cross-version identity.
The public branches are independently buildable today.
Selective artifacts automatically make agents scalable.
The envelope represents complete AEC semantics.
Riff reasoning is already a Speckle primitive.
Human authorization is engineering approval.
The protocol emulator proves production compatibility.
Licensing is the sole access or build blocker.
```

- [ ] **Step 20: Write the questions for Speckle and source notes**

Ask only questions tied to `BT-VALIDATE-001` and `PROTO-001` through `PROTO-003`. Source Notes must restate the observation date, pins, source precedence, and known public-dependency blocker without requesting private material in the document.

- [ ] **Step 21: Validate the Delta structure and commit it alone**

Run:

```text
python -c "from pathlib import Path; p=Path('docs/big-truck-agentic-delta.md'); s=p.read_text(encoding='utf-8'); required=['## Executive Proposition','## The Demonstration','## Big Truck Evidence Ledger','## Big Truck\'s Potential Agentic Delta','## Canonical Evidence and Action Lineage','## Protocol Opportunities','## Permitted and Prohibited Claims','## Questions for Speckle']; missing=[x for x in required if x not in s]; assert not missing, missing; print('delta structure valid')"
python -c "from pathlib import Path; s=Path('docs/big-truck-agentic-delta.md').read_text(encoding='utf-8'); ids=['BT-OBS-001','BT-OBS-002','BT-OBS-003','BT-OBS-004','BT-OBS-005','BT-OBS-006','BT-OBS-007','POC-PROOF-001','BT-HYP-001','BT-VALIDATE-001','PROTO-001','PROTO-002','PROTO-003']; missing=[x for x in ids if x not in s]; assert not missing, missing; print('delta IDs valid')"
python -c "from pathlib import Path; p=Path('docs/big-truck-agentic-delta.md'); bad=[i+1 for i,x in enumerate(p.read_text(encoding='utf-8').splitlines()) if x.endswith((' ', chr(9)))]; assert not bad, bad; print('delta whitespace valid')"
git status --short
```

Expected:

```text
delta structure valid
delta IDs valid
delta whitespace valid
Only docs/big-truck-agentic-delta.md is untracked or modified
```

Commit only the Delta:

```text
git add -- docs/big-truck-agentic-delta.md
git diff --cached --check
git commit -m "docs: define the Big Truck agentic delta"
```

### Task 2: Write the Proof-Gate Roadmap

**Files:**
- Create: `ROADMAP.md`
- Read: `docs/big-truck-agentic-delta.md`
- Read: `docs/superpowers/specs/2026-08-24-speckle-riff-spike-document-design.md`
- Inspect only: `../Riff/**`
- Inspect only: `../Rook/**`

**Interfaces:**
- Consumes: Delta claim IDs, the design's authorization lifecycle, and current repository/runtime observations.
- Produces: a gate-by-gate execution contract that never restates or expands the Delta architecture.

- [ ] **Step 1: Create the Roadmap shell**

Create `ROADMAP.md` with these exact top-level sections:

```markdown
# Speckle–Riff Spike Roadmap

## Target Demonstration
## Scope and Non-Goals
## Current Gate Status
## Reproducible Runtime Baseline
## Gate 0 — Evidence Baseline
## Gate 1 — Canonical Integration Contracts
## Gate 2 — Self-Sufficient Released-Speckle POC
## Gate 3 — Local Big Truck Parity Experiment
## Gate 4 — Conditional Protocol Emulator
## Gate 5 — Optional Speckle Validation
## Verification Matrix
## Risk and Dependency Register
## Upstream Pin and Update Policy
## Promotion Boundary into Riff
## Stop/Go Rules
## Decision Log
```

- [ ] **Step 2: Write the target demonstration and scope boundary**

Use this target demonstration:

```text
One civic-canopy version A supplies bounded project and preliminary Karamba evidence. Chirp proposes one reviewed architectural parameter change. Every Riff node is accepted. The spike captures and verifies one Review Matrix sidecar. The main agent invokes one allowlisted Rook action. Speckle records version B. The spike re-reads B, verifies the exact reviewed rule and stable target identity, then writes one immutable verified or failed AgenticChangeRecord.
```

Copy the specification's explicit non-goals into `## Scope and Non-Goals` without adding implementation work.

- [ ] **Step 3: Initialize the gate-status table**

Use exactly:

```markdown
| Gate | Classification | Initial status | Completion meaning |
| --- | --- | --- | --- |
| 0 | Required POC | in_progress | Evidence sources and the complete runtime are pinned |
| 1 | Required POC | not_started | Transport-neutral contracts and fixtures are validated |
| 2 | Required POC | not_started | The verified A-to-B loop works with released public Speckle capabilities |
| 3 | Post-POC research | not_started | Semantic parity is established or a reproducibility blocker is recorded |
| 4 | Conditional post-POC research | optional | One unresolved Gate-3 protocol question is answered |
| 5 | External validation | optional | Speckle validates or corrects the claimed native seam |
```

- [ ] **Step 4: Capture the source-repository runtime values**

Run these commands and record their exact output and collection date:

```text
git rev-parse HEAD
git -C ../Riff rev-parse HEAD
git -C ../Riff status --short --branch
git -C ../Rook rev-parse HEAD
git -C ../Rook status --short --branch
python --version
```

- [ ] **Step 5: Create the runtime ledger and installed-dependency rows**

Use this schema:

```markdown
| Dependency | Source or installed version | Commit / build | Capture method | Capture date | Status and limitation |
| --- | --- | --- | --- | --- | --- |
```

It must contain rows for:

```text
speckle-riff-spike
Riff and its chirp package
Rook source
installed Rook build
Rhino
Grasshopper
Karamba
released Speckle Rhino/Grasshopper connector
current Speckle API or SDK client
accessible released Speckle service deployment when observable
Python
operating system
all five pinned Big Truck research repositories
```

Use the literal status `not_recorded` when an installed version has not yet been captured. State that Gate 0 cannot complete and Gate 2 cannot begin while any runtime actually used by the demonstration remains `not_recorded`. Do not equate a source commit with an installed plugin build.

- [ ] **Step 6: Record verified values and explicit runtime blockers**

Record these currently observed values only after checking the Step-4 command output:

```text
Riff / chirp source: 21dd4296b33263d26b821c7d43c6fb8394475c4c
Rook source:         a2be88dcd8918f6c87af25ca995c10dbe8044c88
Python:              3.13.5
OS observation:      Microsoft Windows NT 10.0.26200.0
```

If the execution-time values differ, record the actual values and add a dated Decision Log entry; do not force the stale observation into the Roadmap.

- [ ] **Step 7: Write the shared gate template and Gate 0**

Every gate uses this exact shape:

```markdown
### Dependencies
### Work
### Outputs
### Verification
### Exit Criteria
### Claims Newly Permitted
### Stop/Go
```

Gate 0 must require:

```text
- Verify every research-source SHA.
- Record source contradictions using the Delta precedence rule.
- Complete the runtime ledger for every dependency used in the POC.
- Verify the current Riff ReviewMatrix, ReviewPacket, and decision semantics against the design.
- Stop on unexplained dirty source trees or an installed/source mismatch that affects reproducibility.
```

- [ ] **Step 8: Write Gate 1 contract outputs**

Require transport-neutral definitions and schema-valid examples for:

```text
SpeckleVersionRef
SpeckleEvidenceRef
RookActionBinding
agentic_change_candidate
PreflightResult
ReviewMatrixArtifactRef
AgenticChangeRecord
deterministic numeric comparison
```

- [ ] **Step 9: Write the Gate 1 authorization rule**

```text
matrix schema_version == 1.0
AND review_complete == true
AND every node status == accepted
AND exactly one node contains /payload/agentic_change_candidate
AND that node's decision.action == accept
AND source_version, source_canvas_state_fingerprint, target_application_id, parameter_key, before, proposed_after, the complete RookActionBinding, unit, comparison mode absolute_tolerance, and tolerance are copied unchanged into the executor request
AND a fresh source read matches source_version
AND the reviewed binding and fingerprint contract are statically valid
AND the authorization has not already been reserved or consumed
```

Define `RookActionBinding` with producer-observed `GH_Document.DocumentID` as source `canvas_id`, `rook_canonical_ghx_sha256_v1` fingerprint of the complete active document, stable `GH_NumberSlider` instance GUID, literal `value` parameter, Speckle target application ID, parameter key, strict `gh_compare_and_set_value` operation, expected pre-action value, and binding provenance version. Required Rook additions capture the canonical fingerprint during snapshot assembly and, in one UI-thread mutation, recompute it, resolve the reviewed GUID, compare the current decimal value with `before`, and set only `proposed_after`; the request accepts no nickname, range, additional arrays, or alternate control type. Explicitly separate these post-invocation live guards from pre-permit static authorization. Define the one-use `authorization_key` from the matrix hash, authorizing packet, and candidate path. Atomically create the permitted `PreflightResult` at a path derived from snapshot/packet/candidate so concurrent re-exports with different hashes contend for the same file.

- [ ] **Step 10: Write the deterministic numeric and unit rule**

```text
same parameter key
AND same declared unit
AND no implicit unit conversion
AND finite, nonnegative reviewed tolerance
AND abs(decimal(observed) - decimal(authorized)) <= decimal(tolerance)
```

- [ ] **Step 11: Write the Gate 1 refusal cases and exit criteria**

Require preflight refusal for zero or multiple candidates, pending/corrected/rejected nodes, altered sidecar bytes, source-version mismatch, missing/duplicate/malformed reviewed binding, unknown fingerprint algorithm, fingerprint/runtime mismatch, target or cross-field mismatch, unit mismatch, comparison mismatch, unauthorized proposed value, or consumed authorization. These occur before permit creation and create no `AgenticChangeRecord`. After permit creation and invocation, a live document ID, whole-document fingerprint, slider GUID, type, parameter, ambiguity, or `before` mismatch performs no mutation but creates `AgenticChangeRecord.outcome: failed`. Any failure or uncertainty after permit creation requires a new snapshot and review.

- [ ] **Step 12: Write Gate 2 dependencies and work sequence**

Gate 2 dependencies are completed Gates 0 and 1 plus an accessible released Speckle service or self-hosted equivalent, the released connector, the civic-canopy definition, Karamba, Riff/Chirp, the external main agent, and Rook.

Gate 2 work must follow this exact order:

```text
1. Publish or identify version A with explicit stable application IDs.
2. Retrieve bounded evidence through the current Speckle object API or SDK.
3. Confirm the released Grasshopper connector exposes the same state.
4. Capture preliminary Karamba outputs as evidence, not authority.
5. Assemble and submit one immutable Riff reasoning snapshot.
6. Complete every human review.
7. Export one successful Review Matrix response as raw bytes.
8. Write, hash, read back, and verify the sidecar.
9. Copy source_version, source_canvas_state_fingerprint, before, and the complete reviewed RookActionBinding into the executor request.
10. Re-read version A, validate the static fingerprint/binding contract, and prepare the exact reviewed compare-and-set request.
11. Atomically persist the one-use permitted PreflightResult.
12. Invoke one allowlisted gh_compare_and_set_value operation that verifies document ID, complete canvas fingerprint, stable slider GUID, literal value parameter, and live before inside the mutation.
13. Publish version B when execution permits.
14. Re-read B and verify version difference, target identity, and the reviewed numeric rule.
15. Write exactly one immutable AgenticChangeRecord after the executor was invoked, including the authorization key and binding.
```

- [ ] **Step 13: Write Gate 2 verification and exit criteria**

```text
- A and B are distinct immutable Speckle versions when publication succeeds.
- Static authorization completed before permit creation; the Rook receipt proves the complete live canvas fingerprint and before-state were compared atomically with mutation.
- One authorization permit exists and cannot be replayed.
- A compare-and-set identity or value mismatch writes nothing, creates outcome: failed, and cannot be retried.
- The target application ID resolves as intended in B.
- The parameter and unit match the reviewed candidate.
- Verification applies the reviewed deterministic tolerance.
- The matrix artifact hash and byte length revalidate.
- The outcome record is verified only when every check passes.
- Failure after executor invocation produces outcome: failed and preserves B when B exists.
- No claim of structural approval, production readiness, or Big Truck compatibility is made.
```

Reference `POC-PROOF-001` as a reserved claim that may change from `poc_hypothesis` to `proven_locally` only after Gate 2 passes with retained evidence.

- [ ] **Step 14: Write Gate 3 as stoppable local parity research**

Gate 3 must:

```text
- verify public dependencies before attempting bundle generation;
- stop and record the blocker rather than recreate unavailable private schemas;
- use the same canopy evidence questions as the released path;
- require semantic parity before efficiency measurements;
- report the transparent scorecard from BT-HYP-001;
- use scale variants only after the real canopy and only when useful;
- permit either complete or blocked as honest outcomes.
```

- [ ] **Step 15: Write conditional Gate 4**

Gate 4 begins only when Gate 3 names one unresolved protocol question that a local emulator can answer. Its exit criteria state that an emulator result is local evidence, not service compatibility.

- [ ] **Step 16: Write optional Gate 5**

Require:

```text
- be optional;
- list the exact claims and protocol questions sent to Speckle;
- request correction of inaccurate assumptions;
- validate or revise BT-VALIDATE-001 and PROTO-001 through PROTO-003;
- avoid the word certification unless Speckle adopts it;
- leave Gate-2 POC completion unchanged.
```

- [ ] **Step 17: Write the verification matrix**

The verification matrix must contain at least:

```markdown
| Requirement | Gate | Evidence artifact | Pass condition | Failure behavior | Delta reference |
| --- | --- | --- | --- | --- | --- |
```

Cover:

```text
stable source identity
complete accepted review
unique action candidate
exact executor request
deterministic Rook binding
fresh pre-action state
one-use authorization
sidecar byte integrity
preflight refusal
execution failure record
version-B existence
independent B retrieval
numeric and unit verification
released-path evidence parity
Big Truck semantic parity
efficiency measurements
```

- [ ] **Step 18: Write the risk and dependency register**

Include:

```text
unreleased Big Truck drift
unavailable generated schema dependency
released connector versus repository-main confusion
installed/source runtime mismatch
producer-dependent application ID stability
stale or ambiguous Speckle-to-Grasshopper binding
authorization replay or uncertain retry
unit or tolerance mismatch
Riff process-local state loss before sidecar capture
small-model measurement noise
overclaiming professional authority
protocol emulator scope growth
```

- [ ] **Step 19: Write the upstream pin and update policy**

State that upstream changes never silently replace pins. A new SHA requires a dated ledger entry, targeted reinspection of affected claims, and explicit status changes.

- [ ] **Step 20: Write the promotion boundary into Riff**

Use:

```text
May later move into Riff:
- transport-neutral evidence-reference semantics proven useful across integrations
- generic authority or lineage semantics that do not mention Speckle, Grasshopper, Rook, or Karamba

Remains in the spike:
- Speckle transport adapters
- applicationId conventions
- civic-canopy fixtures
- released-versus-Big-Truck comparison harnesses
- local protocol emulator
- AgenticChangeRecord packaging experiments
```

- [ ] **Step 21: Write stop/go rules and the initial decision log**

Stop/go rules must make Gate 0 runtime gaps, Gate 1 authorization failures, Gate 2 failed verification, Gate 3 public-dependency blockers, and Gate 4 lack of a focused question explicit stops. The initial Decision Log records the approved two-document split, Riff-owned semantics, spike-owned persistence, one unique authorizing candidate, post-attempt outcome record, and post-POC Big Truck research classification.

- [ ] **Step 22: Validate Roadmap structure and Delta references, then commit it alone**

Run:

```text
python -c "from pathlib import Path; p=Path('ROADMAP.md'); s=p.read_text(encoding='utf-8'); required=['## Target Demonstration','## Reproducible Runtime Baseline','## Gate 0','## Gate 1','## Gate 2','## Gate 3','## Gate 4','## Gate 5','## Verification Matrix','## Risk and Dependency Register','## Stop/Go Rules']; missing=[x for x in required if x not in s]; assert not missing, missing; print('roadmap structure valid')"
python -c "from pathlib import Path; d=Path('docs/big-truck-agentic-delta.md').read_text(encoding='utf-8'); r=Path('ROADMAP.md').read_text(encoding='utf-8'); refs=['BT-OBS-001','BT-HYP-001','BT-VALIDATE-001','PROTO-001','PROTO-002','PROTO-003']; missing=[x for x in refs if x not in d or x not in r]; assert not missing, missing; print('cross-document references valid')"
python -c "from pathlib import Path; s=Path('ROADMAP.md').read_text(encoding='utf-8'); required=['exactly one','preflight','no `AgenticChangeRecord`','absolute_tolerance','tolerance','not_recorded','installed','source commit']; missing=[x for x in required if x not in s]; assert not missing, missing; print('execution clarifications present')"
python -c "from pathlib import Path; p=Path('ROADMAP.md'); bad=[i+1 for i,x in enumerate(p.read_text(encoding='utf-8').splitlines()) if x.endswith((' ', chr(9)))]; assert not bad, bad; print('roadmap whitespace valid')"
git status --short
```

Expected:

```text
roadmap structure valid
cross-document references valid
execution clarifications present
roadmap whitespace valid
Only ROADMAP.md remains untracked or modified
```

Commit only the Roadmap:

```text
git add -- ROADMAP.md
git diff --cached --check
git commit -m "docs: add the Speckle Riff proof roadmap"
```

### Task 3: Perform the Cross-Document Evidence and Scope Review

**Files:**
- Review: `docs/big-truck-agentic-delta.md`
- Review: `ROADMAP.md`
- Read: `docs/superpowers/specs/2026-08-24-speckle-riff-spike-document-design.md`

**Interfaces:**
- Consumes: both completed documents and the approved specification.
- Produces: a verified two-document package ready for human review; no implementation work.

- [ ] **Step 1: Run the complete structural and terminology verification**

Run:

```text
python -c "from pathlib import Path; files=[Path('docs/big-truck-agentic-delta.md'),Path('ROADMAP.md')]; assert all(p.exists() and p.stat().st_size>0 for p in files); print('documents exist')"
python -c "from pathlib import Path; d=Path('docs/big-truck-agentic-delta.md').read_text(encoding='utf-8'); r=Path('ROADMAP.md').read_text(encoding='utf-8'); required=['observed_upstream','proven_locally','poc_hypothesis','requires_speckle_validation']; missing=[x for x in required if x not in d]; assert not missing, missing; assert 'Gates 0–2' in r or 'Gates 0-2' in r; assert 'Gate 5' in r and 'optional' in r.lower(); print('evidence and gate language valid')"
python -c "from pathlib import Path; d=Path('docs/big-truck-agentic-delta.md').read_text(encoding='utf-8'); marker='## Permitted and Prohibited Claims'; assert marker in d; section=d.split(marker,1)[1].split('\n## ',1)[0].lower(); required=['universally guarantees cross-version identity','human authorization is engineering approval','protocol emulator proves production compatibility']; missing=[x for x in required if x not in section]; assert not missing, missing; print('prohibited-claims section structurally valid')"
git diff --check 7726b57b1e6f116ef8e41518411b7dfc9498e24a HEAD
git status --short --branch
```

Expected:

```text
documents exist
evidence and gate language valid
prohibited-claims section structurally valid
No diff-check output
The worktree is clean because the approved plan and both documents are committed
```

- [ ] **Step 2: Audit the evidence ledger claim states and citations**

For every ledger row, verify:

```text
1. The evidence state is explicit.
2. observed_upstream has a pinned primary-source permalink.
3. proven_locally has a retained local artifact; before Gate 2, no POC behavior uses this state.
4. poc_hypothesis names its measurement.
5. requires_speckle_validation names the unresolved external question.
6. Contradictory upstream sources are both visible.
```

- [ ] **Step 3: Audit the Delta interpretation and proposal sections**

Review these sections:

```text
Big Truck's Potential Agentic Delta
Temporary-to-Native Replacement Map
Protocol Opportunities
Questions for Speckle
```

Verify that every agentic consequence is a measured hypothesis unless proven, every opportunity remains a question, and prohibited statements occur only as explicit prohibitions or limitations.

- [ ] **Step 4: Audit Roadmap claim references and execution boundaries**

Verify that every Delta ID used by the Roadmap exists, Gate 2 is the independent POC completion gate, Gates 3–5 are post-POC, runtime gaps block Gate 0, and no gate instructs the documentation executor to implement the POC.

- [ ] **Step 5: Apply the smallest corrections and rerun structural verification**

If an audit item fails, edit only the affected paragraph or table, rerun Task 3 Step 1, and commit only the two document files with:

```text
git add -- docs/big-truck-agentic-delta.md ROADMAP.md
git diff --cached --check
git commit -m "docs: tighten Speckle evidence claims"
```

- [ ] **Step 6: Have an independent reviewer check the final documents against the specification**

Give the reviewer these exact questions:

```text
1. Does any sentence claim unreleased Big Truck behavior as settled fact?
2. Does the Delta remain a proposition rather than a backlog?
3. Does the Roadmap remain executable without duplicating the Delta?
4. Is Gate 2 independent of private Speckle and Big Truck access?
5. Are Gates 3–5 clearly post-POC and stoppable?
6. Is the authorizing node unique and non-overridable?
7. Are preflight refusal and failed authorized execution distinct?
8. Are numeric and unit comparisons deterministic?
9. Is the complete runtime ledger required before Gate 2?
10. Does any proposed Riff change or product-code work leak into this documentation slice?
```

- [ ] **Step 7: Apply verified reviewer corrections and rerun Task 3 Step 1**

Apply only technically verified corrections that remain within the approved specification. If files change, commit only the two document files using the Task 3 Step 5 commit sequence.

- [ ] **Step 8: Produce the final human-review report and stop**

Run:

```text
git log --oneline --decorate -5
git status --short --branch
git diff --check
git diff --name-only 7726b57b1e6f116ef8e41518411b7dfc9498e24a..HEAD
```

Report:

```text
- Files created
- Exact commits
- Upstream revisions inspected
- Runtime values recorded and any not_recorded blockers
- Claim IDs added
- Structural and diff-check command results
- Reviewer verdict and corrections
- Any deviation from the specification
```

Stop for human approval. Do not execute Gate 0, build the POC, push, open a pull request, or modify Riff.
