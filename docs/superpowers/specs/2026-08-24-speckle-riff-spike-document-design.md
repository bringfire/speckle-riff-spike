# Speckle–Riff Spike Documentation Design

**Status:** Approved
**Date:** 2026-08-24
**Repository:** `speckle-riff-spike`
**Outputs governed by this design:**

- `docs/big-truck-agentic-delta.md`
- `ROADMAP.md`

## 1. Purpose

This specification governs two documents that define and sequence a Speckle–Riff proof of concept. The work tests a specific proposition:

> Speckle makes versioned project evidence available to agents. Riff makes agent reasoning available to humans and makes human authority consequential.

The proof of concept does not compete with Speckle's project-data infrastructure. It demonstrates a reasoning, review, authorization, and lineage layer that Speckle's versioned project state makes possible and increasingly necessary as agents begin acting in AEC workflows.

The documents must be bold enough to establish that proposition and precise enough for Speckle's technical and product leadership to scrutinize. They must separate demonstrated behavior from upstream observations, hypotheses, and capabilities that require Speckle validation.

## 2. Document and Repository Boundary

The documentation belongs in the public `speckle-riff-spike` repository.

### Big Truck Agentic Delta

`docs/big-truck-agentic-delta.md` is the durable Speckle-facing technical proposition. It explains the product thesis, demonstrated loop, observed Big Truck direction, measurable agentic delta, limitations, and focused opportunities for collaboration.

It contains no implementation backlog, schedule, or task checklist.

### Roadmap

`ROADMAP.md` is the executable research sequence. It defines proof gates, required artifacts, verification, risks, upstream pins, stop/go conditions, and the boundary between disposable spike work and contracts that might later be promoted into Riff.

It links to the Delta document rather than repeating the technical argument.

### Riff

No Riff files or contracts change during this documentation work. Riff remains domain-neutral. It should eventually receive only a concise link to the spike and any transport-neutral contract that survives practical validation.

## 3. Product and Authority Boundary

The systems have distinct responsibilities:

```text
Speckle
→ versioned project state, object identity, properties, relationships, and transport

Karamba
→ deterministic preliminary structural calculations and reported results

Chirp
→ structured interpretation, assumptions, proposals, uncertainty, and provenance

Riff
→ inspectable reasoning, prioritization, human review, and immutable decisions

External main agent
→ orchestration and assembly of evidence, reasoning, and authorized intent

Rook
→ one narrowly allowlisted Grasshopper action after authorization

speckle-riff-spike
→ transport seam, durable lineage, verification, and comparative experiments
```

The documents must distinguish:

- deterministic calculation from agent interpretation;
- Riff priority from human decisions;
- authorization of an architectural study action from structural or professional approval;
- an agent's proposed change from execution of that change;
- successful execution from verified outcome;
- immutable semantics owned by Riff from durable packaging owned by the spike.

Agents do not supersede engineering judgment or deterministic analysis. Karamba is preliminary advisory evidence. Chirp may reason over its results. A human may authorize an architectural exploration, but that authorization is not engineering approval.

## 4. Self-Sufficient POC

The POC uses publicly available released Speckle capabilities. It completes without private Speckle access, unreleased Big Truck access, Speckle collaboration, an Enterprise workspace, or Speckle Automate. Riff and the spike run as external processes against ordinary released APIs and connector operations; direct orchestration, polling, or standard server webhooks may trigger work without changing the transport-neutral reasoning and authorization contracts. Speckle Automate may be evaluated later as an optional deployment adapter, but it is not part of Riff's core architecture or the POC dependency chain.

The target workflow is:

```text
Speckle version A
→ retrieve bounded project evidence
→ include preliminary Karamba results as deterministic evidence
→ Chirp produces structured interpretation and an exact action candidate
→ Riff presents the reasoning and records human decisions
→ export, persist, and verify the complete Review Matrix authorization artifact
→ external main agent and Rook perform one allowlisted architectural change
→ publish Speckle version B
→ re-read B and deterministically verify the authorized change
→ publish one immutable AgenticChangeRecord
```

The change is one architectural parameter informed, but never automatically dictated, by Karamba evidence. A likely example is canopy bay or support spacing. Structural member sizing and autonomous optimization are outside this slice.

The POC is complete at the verified A-to-B loop and durable lineage artifact. Later Big Truck experiments and Speckle validation are separate research gates.

## 5. Riff Compatibility and Authorization Policy

The current Riff implementation already provides the required domain-neutral primitives:

- `canvas_id`, `snapshot_id`, and `run_id`;
- ordered nodes with stable producer-supplied `node_id` values;
- complete immutable `ReviewPacket` objects;
- node-to-`packet_id` mappings;
- per-node terminal decisions and reviewer attribution;
- immutable Riff annotations with grounded source references;
- an atomically observed Review Matrix export;
- arbitrary strict JSON in `ReviewPacket.payload`.

No Riff schema or code change is required.

### Review completion is not authorization

Riff defines `review_complete` as no node remaining pending. It does not mean that the reasoning was accepted. A matrix containing rejected or correction-requested nodes can be complete.

The POC execution policy has two explicit phases. Static authorization is evaluated before permit creation:

```text
review_complete is true
AND every node status is accepted
AND exactly one node contains payload.agentic_change_candidate
AND the designated authorizing packet decision is accept
AND source_version is re-read and still names the reviewed immutable Speckle state
AND the complete RookActionBinding is schema-valid and cross-field consistent
AND the authorization has not already been reserved or consumed
AND the attempted action exactly matches the reviewed action candidate
```

Only after these checks may the spike create the one-use permit. Live execution guards are then evaluated inside the invoked Rook mutation:

```text
active GH_Document.DocumentID matches source_canvas_id
AND the recomputed whole-document fingerprint matches source_canvas_state_fingerprint
AND the stable InstanceGuid resolves to exactly one GH_NumberSlider
AND the parameter is the literal value
AND the live value exactly equals before
```

A static check failure is a preflight refusal with no `AgenticChangeRecord`. A live execution-guard failure occurs after permit creation and invocation, performs no mutation, creates `AgenticChangeRecord.outcome: failed`, and cannot be retried.

Any `pending`, `correction_requested`, or `rejected` node blocks execution. Correction is terminal for its immutable packet; revision requires a new snapshot and new review records.

Riff annotations, including `change_candidate`, are advisory. They can explain or prioritize review but can never authorize execution.

### Reviewed action candidate

The authorizing node's existing `ReviewPacket.payload` contains a spike-owned candidate without changing Riff's schema:

```json
{
  "agentic_change_candidate": {
    "source_version": {
      "server_origin": "https://example.speckle.systems",
      "project_id": "project-id",
      "model_id": "model-id",
      "version_id": "version-a"
    },
    "target_application_id": "canopy-bay-07",
    "parameter_key": "canopy_bay_spacing",
    "before": 2.4,
    "proposed_after": 2.9,
    "unit": "m",
    "rook_action_binding": {
      "schema_version": "1.0",
      "binding_id": "canopy-spacing-control",
      "source_canvas_id": "aaaaaaaa-bbbb-cccc-dddd-eeeeeeeeeeee",
      "source_canvas_state_fingerprint": {
        "algorithm": "rook_canonical_ghx_sha256_v1",
        "sha256": "0123456789abcdef0123456789abcdef0123456789abcdef0123456789abcdef"
      },
      "grasshopper_component_instance_id": "11111111-2222-3333-4444-555555555555",
      "control_type": "GH_NumberSlider",
      "input_or_parameter_id": "value",
      "target_application_id": "canopy-bay-07",
      "parameter_key": "canopy_bay_spacing",
      "allowed_rook_operation": "gh_compare_and_set_value",
      "expected_pre_action_value": 2.4,
      "binding_provenance_version": "canopy-binding-v1"
    },
    "comparison": {
      "mode": "absolute_tolerance",
      "tolerance": 0.001
    }
  }
}
```

Exactly one node in the authoritative Review Matrix may contain `payload.agentic_change_candidate`. That unique node is the authorizing node; the executor does not accept a caller-selected override. Zero candidates or multiple candidates are preflight refusals.

"Exactly matches" means that `source_version`, target application ID, parameter key, `before`, proposed value, declared unit, the complete `rook_action_binding`, comparison mode, and tolerance supplied to execution are copied unchanged from that candidate. The POC performs no implicit unit conversion. Numeric verification converts the authorized value, observed value, and tolerance from their JSON textual representations to decimal values and passes only when `abs(observed - authorized) <= tolerance`. The tolerance must be finite, nonnegative, explicitly reviewed, and expressed in the same declared unit. A zero tolerance expresses exact decimal equality.

`RookActionBinding` is the spike-owned, transport-neutral seam between a Speckle action target and one Grasshopper control. The stable `grasshopper_component_instance_id` must come from Grasshopper instance identity, never a label, position, list index, nickname, or role. For this POC, `source_canvas_id` is the canonical string form of the producer-observed Grasshopper `GH_Document.DocumentID`; a reopened definition with a different document ID requires a new snapshot and review. The binding is restricted to `control_type: GH_NumberSlider`, `input_or_parameter_id: value`, and the strict operation literal `gh_compare_and_set_value`.

`source_canvas_state_fingerprint` is produced by a required Rook capture operation when the reasoning snapshot is assembled. `rook_canonical_ghx_sha256_v1` means SHA-256 over Rook's code-owned canonical in-memory GHX serialization of the complete active `GH_Document` using the pinned Grasshopper runtime. Canonicalization must normalize or explicitly exclude volatile metadata and nondeterministic ordering. Repeated captures of an unchanged document must produce byte-identical canonical GHX and the same SHA-256, and a no-op Grasshopper solution or recompute must not change either result. Snapshot capture and execution-time recomputation must invoke the same versioned Rook code path on the Grasshopper UI thread with the same pinned Rook and Grasshopper runtimes. Cosmetic state may be included and cause a conservative mismatch; selection, viewport zoom, and other state absent from GHX are outside the execution state. Gate 1 must prove both invariance under repeated unchanged captures and a no-op solution/recompute, and sensitivity to object addition/removal, wiring, persistent control values, script source, and component/pin configuration. An unknown algorithm, code-path version, capture-time thread context, or runtime-version mismatch refuses preflight. A wrong execution thread discovered only after Rook invocation performs no mutation and is a failed authorized attempt.

`gh_compare_and_set_value` is a required POC Rook capability, not a claim about the currently inspected Rook runtime. In one Rhino/Grasshopper UI-thread operation it must require the reviewed document ID, source-state fingerprint, and component `InstanceGuid`; recompute and compare the complete document fingerprint before any write; find exactly one `GH_NumberSlider`; compare its current decimal value with the reviewed `before` value; and set only its value to `proposed_after` when every guard succeeds. Its request contains exactly the document ID, fingerprint algorithm and SHA-256, component instance GUID, literal parameter `value`, expected value, proposed value, and authorization key; it accepts no nickname, minimum, maximum, additional edit arrays, or alternate control type. It returns those identities, the recomputed fingerprint, and the observed before/after values in a receipt. These mutation-bound guards close the time-of-check/time-of-use windows that an ordinary `gh_snapshot` followed by `gh_edit.set_values` cannot close. Gate 2 cannot begin until the installed Rook runtime supplies and verifies the capture and compare-and-set operations.

The reviewed binding is schema-valid only when its source canvas equals the Review Matrix `canvas_id`; its source-state fingerprint uses the supported algorithm and a 64-character lowercase hexadecimal SHA-256; its target application ID and parameter key exactly equal the candidate fields; its expected pre-action value exactly equals `before`; and its provenance version is the reviewed immutable binding revision. A missing, duplicate, malformed, unknown-algorithm, runtime-mismatched, or cross-field-mismatched reviewed binding is a preflight refusal. Immediately before invoking Rook, the executor re-reads version A and verifies the reviewed source-version identity and target. After permit creation and invocation, the mutation-bound Rook operation validates its Grasshopper UI-thread context, the live document fingerprint, control identity, type, parameter, and exact decimal equality with `before` before writing. A wrong execution thread or live document-state, target, or `before` mismatch performs no mutation but is a failed authorized attempt: it creates `AgenticChangeRecord.outcome: failed` and cannot be retried. No tolerance or implicit conversion is used for this freshness check.

### One-use authorization and retry policy

The spike derives an `authorization_key` as SHA-256 over compact, key-sorted UTF-8 JSON containing exactly `review_matrix_sha256`, `authorizing_packet_id`, and `candidate_field_path`. After every sidecar, source-version, and binding check passes—and immediately before the Rook invocation—the executor atomically and exclusively persists a permitted `PreflightResult` containing that key. Creating that immutable permit consumes the authorization for one possible attempt. Concurrent creation or any existing permit for the same key is a refusal.

Because a new Review Matrix export changes `exported_at` and therefore may change the sidecar hash, the exclusive permit location is derived from the canonical tuple `(snapshot_id, authorizing_packet_id, candidate_field_path)`, not from `authorization_key`. The permit stores the key and matrix hash. This makes the uniqueness check and creation one atomic filesystem operation across concurrent re-exports with different hashes; there is no separate lookup-then-create window. A refusal before permit creation may be retried only while the same reviewed artifact still matches the live state. A stale source version, stale `before`, stale binding, any failure after permit creation, or any uncertain invocation outcome requires a new Chirp snapshot and new human review; the old authorization is never retried.

The outcome record cites the exact reviewed value using:

```text
snapshot_id
authorizing_node_id
authorizing_packet_id
candidate_field_path: /payload/agentic_change_candidate
authorization_key
```

The packet's ordinary `parameters[]` may also expose the proposed value and source for human readability, but it does not replace the exact target-bearing payload candidate.

## 6. Identity Namespaces

The POC must keep these identities separate:

```text
canvas_id                 Grasshopper definition
snapshot_id               one immutable reasoning capture/import
run_id                    one Chirp reasoning run
node_id/component_id      stable Chirp/Grasshopper component instance
packet_id                 one Riff human-review record
Speckle applicationId     one project object or action target
Speckle version ID        one immutable project state
```

The canopy producer supplies explicit application IDs and verifies their continuity from A to B. This is a tested POC invariant, not a claim that Big Truck or Speckle universally guarantees stable cross-version identity.

## 7. Durable Authorization Sidecar

Riff owns reasoning, review, and decision semantics. Its current prototype storage is process-local. The spike owns durable sidecar capture, cryptographic binding, execution lineage, and verification artifacts.

Before any action begins, the spike must:

1. request one current Review Matrix;
2. require a successful and complete HTTP response with `schema_version: "1.0"`;
3. treat the raw UTF-8 response body as the authoritative artifact;
4. write those bytes unchanged to an immutable sidecar path;
5. calculate SHA-256 and byte length from the exact bytes;
6. read the file back and verify its byte length and SHA-256;
7. validate the conservative authorization policy against that matrix;
8. permit execution only after every check passes.

A failed or incomplete fetch produces no authorization artifact and permits no execution. The implementation must not parse and reserialize the response before hashing. The digest identifies one exact exported artifact, not every semantically equivalent matrix export.

The sidecar reference records:

```text
relative_path
sha256
byte_length
media_type
review_matrix_schema_version
```

Riff's `exported_at` is the atomic observation time of review state. It is not the action authorization time, sidecar write time, or version-B publication time.

The JSON sidecar is a POC packaging decision, not a permanent product boundary. The durable logical requirement is immutable authorization evidence, immutable post-attempt outcome, and a cryptographic binding between them. Future JSON, Parquet, or Big Truck packaging remains unresolved.

One sanitized golden Review Matrix and matching `AgenticChangeRecord` are committed as an inspectable example and regression fixture. Ordinary generated run outputs remain untracked.

## 8. AgenticChangeRecord

The Review Matrix proves prior human authorization. One `AgenticChangeRecord` is created after the authorized action attempt and never mutated afterward.

Authorization and sidecar checks are preflight. A failed preflight performs no action and creates no `AgenticChangeRecord`; the refusal is retained as test output or a minimal spike-owned preflight result. Once authorization passes and the executor is invoked, execution, publication, or verification failure produces an immutable `AgenticChangeRecord` with `outcome: failed`.

Conceptually:

```text
AgenticChangeRecord
├── schema_version
├── record_id
├── created_at
├── outcome: verified | failed
├── source_version
│   ├── server_origin
│   ├── project_id
│   ├── model_id
│   └── version_id
├── source_evidence[]
│   ├── application_id
│   ├── field_path
│   └── observed_value
├── authorization
│   ├── canvas_id
│   ├── snapshot_id
│   ├── run_id
│   ├── authorizing_node_id
│   ├── authorizing_packet_id
│   ├── candidate_field_path
│   ├── authorization_key
│   ├── review_matrix_path
│   ├── review_matrix_sha256
│   ├── review_matrix_byte_length
│   ├── review_matrix_media_type
│   └── review_matrix_schema_version
├── authorized_change
│   ├── target_application_id
│   ├── parameter
│   ├── before
│   ├── after
│   ├── unit
│   ├── comparison
│   └── rook_action_binding
│       ├── schema_version
│       ├── binding_id
│       ├── source_canvas_id
│       ├── source_canvas_state_fingerprint
│       │   ├── algorithm
│       │   └── sha256
│       ├── grasshopper_component_instance_id
│       ├── control_type
│       ├── input_or_parameter_id
│       ├── target_application_id
│       ├── parameter_key
│       ├── allowed_rook_operation
│       ├── expected_pre_action_value
│       └── binding_provenance_version
├── execution
│   ├── actor
│   ├── tool
│   ├── attempted_at
│   ├── result_version?
│   └── safe_failure?
└── verification
    ├── checked_at
    ├── expected
    ├── observed
    ├── passed
    └── evidence_references[]
```

Constraints:

- Exactly one allowlisted parameter change appears in a record.
- The source version, pre-action value, selected binding, copied change, declared unit, and comparison rule must exactly match the reviewed payload candidate.
- The authorization key and complete selected binding appear unchanged in the executor request and outcome record.
- `result_version` is present whenever a published version was observed, including when later verification fails.
- `outcome: verified` requires every deterministic check to pass.
- `outcome: failed` may include or omit version B depending on where failure occurred.
- Safe failure details do not contain credentials, private exceptions, prompts, or stack traces.
- Publication of a version ID alone never implies success.
- The record encoding is a POC choice; the logical contract is packaging-independent.

## 9. Verification and Failure Model

The required POC acceptance sequence is:

1. Version A contains explicit, testable application IDs.
2. The current Speckle API or SDK retrieves the required architectural and Karamba evidence.
3. Chirp's reviewed packet contains the exact action candidate.
4. The Riff Review Matrix is complete and every node is accepted.
5. The raw matrix sidecar is written, read back, and cryptographically verified.
6. Version A and the reviewed `RookActionBinding` are revalidated immediately before action; the complete live canvas fingerprint and `before` value are enforced atomically by the Rook mutation.
7. One authorization key is atomically reserved and cannot be replayed.
8. Rook atomically compares and changes exactly one allowlisted slider value through the resolved binding.
9. A distinct version B is published.
10. Version B is re-read rather than trusted from the publish response.
11. The target application ID resolves as intended in B.
12. The observed value satisfies the human-authorized deterministic comparison rule in the declared unit.
13. One immutable `AgenticChangeRecord` binds A, authorization, binding, action, B, and verification.

Required negative demonstrations are:

- a pending review blocks execution;
- correction or rejection blocks execution;
- zero or multiple action candidates block execution;
- an action-candidate mismatch blocks execution;
- a source-version mismatch or invalid reviewed binding refuses before permit creation;
- a live document ID, whole-document fingerprint, target, type, parameter, or `before` mismatch performs no mutation but produces a failed post-invocation record;
- a consumed authorization key or a second permit for the same reviewed candidate blocks execution;
- a missing, incomplete, or modified Review Matrix blocks execution;
- unstable or missing target identity fails verification;
- a published B with the wrong value produces `outcome: failed` while retaining its version reference;
- network, service, or tool failure never becomes inferred success;
- a failed authorization or preflight produces no action and no `AgenticChangeRecord` while retaining refusal evidence;
- an authorized attempt that fails during execution, publication, or verification produces a safe immutable outcome record;
- an uncertain or failed attempt is never retried from the same reviewed snapshot.

## 10. Evidence Discipline

Every material Big Truck claim carries exactly one evidence state:

```text
observed_upstream
proven_locally
poc_hypothesis
requires_speckle_validation
```

Each upstream observation records:

- repository;
- branch;
- commit SHA;
- observation date;
- source file, executable code, or test;
- known contradiction or superseded material.

Source precedence is:

```text
executable code and tests at the pinned SHA
→ current handoff documents
→ planning documents
→ our interpretation or hypothesis
```

Contradictions remain visible rather than being silently reconciled.

The initial inspected revisions are:

| Upstream | Branch | Commit |
| --- | --- | --- |
| `speckle-sharp-sdk` | `big-truck` | `f87d39cff9f54aff6c30b634780c834ba070ff4e` |
| `speckle-sharp-connectors` | `big-truck` | `0313a89878d5d91c7b69e0492da4dd7b6c76b51d` |
| `speckle-server` | `main` | `51d43b91c4681a75bff8b285da7f443a4599da67` |
| `specklepy` | `main` | `5481458ecbae39f357f247deb33cb4976000e966` |
| `speckle-docs` | `main` | `5d88e384b62688a9b0443ad72b13069b7b16e639` |

This table is a Big Truck research-source ledger, not the complete POC runtime baseline. The Roadmap must also record the exact Riff and Chirp commit, Rook commit or release, Rhino and Grasshopper versions, Karamba version, released Speckle connector version, current Speckle API or SDK client version, service deployment/version when observable, operating system, and language runtimes used for every reproducible POC result. A released connector version and a repository `main` commit must never be treated as equivalent without evidence.

The documents must not claim that:

- a mutable public branch is the final Big Truck specification;
- Big Truck universally guarantees cross-version identity;
- the public integration is independently buildable today;
- selective artifacts automatically make agents scalable;
- emitted topology represents complete AEC semantics;
- Riff reasoning is already a Speckle primitive;
- human authorization constitutes engineering approval;
- licensing is the sole current access or build blocker.

Big Truck performance and context-reduction benefits become affirmative claims only after measurement.

## 11. Comparative Experiment

The non-Big-Truck baseline uses the current Speckle object API or SDK for controlled instrumentation. The released Grasshopper connector provides one end-to-end sanity check that the same source state is accessible in the design environment.

The local Big Truck experiment must answer the same predefined canopy evidence questions. Semantic correctness is the gate. Efficiency results matter only after parity is demonstrated.

The transparent measurement scorecard is:

- evidence facts resolved correctly;
- identity and relationship references preserved;
- bytes transferred or read;
- objects and geometry materialized;
- elapsed retrieval time;
- normalized evidence size and resulting model-input tokens.

There is no opaque composite score. Results are reported directly and are not extrapolated into unsupported production claims.

The real civic-canopy model is the primary test. If it is too small to expose an interpretable difference, one or two deterministic scale variants may repeat its evidence structure with unique stable IDs. Scale variants run only after the real loop passes and must not become a separate project.

## 12. Roadmap Proof Gates

### Gate 0 — Evidence baseline

Pin upstream repositories and revisions, establish the source ledger, record contradictions, and capture the complete reproducible POC runtime-baseline ledger. No capability claim exceeds inspected evidence.

### Gate 1 — Canonical integration contracts

Define evidence references, action-candidate convention, `RookActionBinding`, live pre-action invariants, one-use authorization policy, sidecar binding, and immutable outcome record independently of transport.

### Gate 2 — Self-sufficient released-Speckle POC

Complete the civic-canopy A-to-B loop using publicly available released Speckle capabilities. This is the POC completion gate.

### Gate 3 — Local Big Truck parity experiment

Attempt bundle generation and consumption only when the pinned public Big Truck dependencies are reproducible. If private or unavailable generated dependencies remain required, record the blocker and stop without recreating private schemas. When the experiment can run, require semantic parity before reporting bounded-read measurements. This is independently stoppable post-POC research.

### Gate 4 — Conditional protocol-emulator round trip

Build a narrowly scoped local emulator only if Gate 3 exposes a protocol question that the emulator can answer. It is not a default miniature-server project and never proves compatibility with an unreleased production service.

### Gate 5 — Optional Speckle validation

Test with Speckle-provided infrastructure or guidance and revise interoperability claims and Protocol Opportunities. This external gate does not determine whether the independent POC is complete.

Each Roadmap gate must list:

- dependencies;
- work;
- outputs;
- verification;
- exit criteria;
- claims newly permitted;
- stop/go conditions.

Gates 0–2 are required for the POC. Gates 3–4 are independently stoppable post-POC research. Gate 5 is optional external Speckle validation.

## 13. Protocol Opportunities

The Delta document contains a bounded register of evidence-driven questions, not a product wishlist or inferred Speckle backlog.

Each entry contains:

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

The initial register is capped at three candidates:

1. **Identity continuity metadata** — whether producers could declare how an application ID was established and whether it is expected to persist across versions.
2. **Grounded derived-evidence references** — whether analysis artifacts could cite source version, application ID, relationship, and field-level evidence through a stable convention.
3. **Artifact capability discovery** — whether consumers could determine which schemas, relation types, and evidence categories a bundle contains without private or out-of-band knowledge.

These are proposals, not claims or requirements. Entries may be revised or retired if experiments show that Big Truck already addresses them or that they are unnecessary.

## 14. Explicit Non-Goals

The two documents must not expand the POC into:

- autonomous continuous optimization;
- automatic engineering approval;
- unrestricted Grasshopper modification;
- a generalized Speckle connector replacement;
- production persistence or deployment infrastructure;
- backwards compatibility across Speckle generations;
- a Riff geometry or BIM data store;
- Speckle-specific changes to Riff's Review Matrix;
- live Big Truck dependence for the self-sufficient POC;
- a protocol emulator without a question established by the parity experiment;
- a synthetic performance-benchmarking program;
- an assertion of unobserved or unvalidated Big Truck behavior.

## 15. Required Delta Structure

`docs/big-truck-agentic-delta.md` will contain:

1. Executive thesis
2. Independent-project disclaimer
3. Civic-canopy POC narrative
4. Current released-Speckle baseline
5. Big Truck observations at pinned revisions
6. Evidence taxonomy and source ledger
7. Agentic delta by capability
8. Canonical evidence and `AgenticChangeRecord` seam
9. Identity guarantees and limitations
10. Speckle, Chirp, Riff, Rook, Karamba, and spike ownership
11. Temporary-to-native replacement map
12. Measurement strategy
13. Bounded Protocol Opportunities register
14. Claims permitted and prohibited
15. Questions and eventual collaboration requests for Speckle

Technical evidence should use compact tables or appendices so the audience encounters the thesis and demonstrated loop before implementation detail.

## 16. Required Roadmap Structure

`ROADMAP.md` will contain:

1. Final demonstration and success condition
2. Scope and explicit non-goals
3. Gates 0–5
4. Deliverables and verification per gate
5. Verification matrix
6. Risk and dependency register
7. Reproducible runtime-baseline ledger
8. Upstream pin and update policy
9. Promotion boundary into Riff
10. Stop/go conditions
11. Current status and decision log

The Roadmap should reference stable Delta claim or evidence IDs instead of repeating capability arguments.

## 17. Documentation Acceptance

The documentation work is acceptable only when:

- every material Big Truck claim has an evidence state and pinned provenance;
- contradictory upstream material is visible and source precedence is applied;
- Gate 2 is defined to complete without private Speckle or unreleased Big Truck access;
- Gates 3–5 remain post-POC and independently stoppable;
- the Delta contains no execution backlog;
- the Roadmap does not duplicate the Delta argument;
- the POC authority and professional-liability boundaries are explicit;
- the current Riff contract is described accurately and remains unchanged;
- the authorizing node is selected uniquely and cannot be overridden by the executor;
- the reviewed source version, whole-document fingerprint, `before`, and complete `RookActionBinding` are copied; static source/binding checks occur before permit creation and all live guards are compared atomically with mutation;
- invalid reviewed bindings refuse preflight, while live identity/value mismatches fail safely after invocation; neither path falls back to labels, positions, or indexes;
- one authorization can permit at most one possible attempt, and retry after failure or uncertainty requires a new snapshot and review;
- preflight refusal is distinguished from a failed authorized attempt;
- numeric and unit comparison rules are explicit and deterministic;
- the complete POC runtime, not only research repositories, is required to be pinned;
- the POC sidecar is described as temporary packaging rather than a permanent product boundary;
- proposed protocol changes are clearly separated from observed upstream behavior;
- no implementation, harness, emulator, or POC code is introduced as part of writing these documents.
