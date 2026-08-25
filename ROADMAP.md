# Speckle–Riff Spike Roadmap

This is the executable proof-gate contract for the independent research spike. It consumes the approved [Big Truck Agentic Delta](docs/big-truck-agentic-delta.md) by stable claim ID; it does not replace its technical argument or assert Speckle compatibility.

## Target Demonstration

One civic-canopy version A supplies bounded project and preliminary Karamba evidence. Chirp proposes one reviewed architectural parameter change. Every Riff node is accepted. The spike captures and verifies one Review Matrix sidecar. The main agent invokes one allowlisted Rook action. Speckle records version B. The spike re-reads B, verifies the exact reviewed rule and stable target identity, then writes one immutable verified or failed AgenticChangeRecord.

`POC-PROOF-001` remains `poc_hypothesis` until this Gate-2 demonstration passes with retained evidence; it may then change to `proven_locally`.

## Scope and Non-Goals

The POC uses released public Speckle capabilities, one bounded architectural parameter change, and preliminary Karamba evidence. Human authorization of an architectural exploration is not professional engineering approval. The two documents must not expand the POC into:

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

## Current Gate Status

| Gate | Classification | Initial status | Completion meaning |
| --- | --- | --- | --- |
| 0 | Required POC | in_progress | Evidence sources and the complete runtime are pinned |
| 1 | Required POC | not_started | Transport-neutral contracts and fixtures are validated |
| 2 | Required POC | not_started | The verified A-to-B loop works with released public Speckle capabilities |
| 3 | Post-POC research | not_started | Semantic parity is established or a reproducibility blocker is recorded |
| 4 | Conditional post-POC research | optional | One unresolved Gate-3 protocol question is answered |
| 5 | External validation | optional | Speckle validates or corrects the claimed native seam |

Gates 0–2 are the required POC. Gates 3–5 are post-POC and independently stoppable; Gate 5 is optional. Gate 2 completes independently of Gates 3–5.

## Reproducible Runtime Baseline

Collected on 2026-08-25 from the source repositories and the executing host. These observations are a baseline ledger, not evidence that an installed runtime is reproducible.

```text
> git rev-parse HEAD
record the executing package commit in the external Gate-0 run ledger

> git -C ../Riff rev-parse HEAD
21dd4296b33263d26b821c7d43c6fb8394475c4c

> git -C ../Riff status --short --branch
## main...origin/main
?? GH/
?? Presentation/
?? Screenshots/
?? Video/
?? traces/

> git -C ../Rook rev-parse HEAD
a2be88dcd8918f6c87af25ca995c10dbe8044c88

> git -C ../Rook status --short --branch
## main...origin/main [ahead 8, behind 164]

> python --version
Python 3.13.5
```

Host operating-system observation collected on 2026-08-25: `Microsoft Windows NT 10.0.26200.0`.

| Dependency | Source or installed version | Commit / build | Capture method | Capture date | Status and limitation |
| --- | --- | --- | --- | --- | --- |
| speckle-riff-spike | checked-in package | recorded externally for each approved run; not self-pinned here | `git rev-parse HEAD` at Gate-0 execution | 2026-08-25 | this Roadmap and `docs/big-truck-agentic-delta.md` are the package sources; no POC execution recorded |
| Riff and its chirp package | source checkout | `21dd4296b33263d26b821c7d43c6fb8394475c4c` | `git -C ../Riff rev-parse HEAD` | 2026-08-25 | source observed; tree is dirty with untracked `GH/`, `Presentation/`, `Screenshots/`, `Video/`, and `traces/` |
| Rook source | source checkout | `a2be88dcd8918f6c87af25ca995c10dbe8044c88` | `git -C ../Rook rev-parse HEAD` and status | 2026-08-25 | source observed; `main` is ahead 8 and behind 164 of `origin/main`; inspected `gh_snapshot`/`gh_edit.set_values` cannot provide a canonical whole-document token or stable-GUID atomic compare-and-set, so fingerprint capture and `gh_compare_and_set_value` remain Gate-1/2 prerequisites |
| installed Rook build | `not_recorded` | `not_recorded` | installed-build capture not yet performed | 2026-08-25 | installed source mismatch is unknown; a source commit is not an installed plugin build |
| Rhino | `not_recorded` | `not_recorded` | installed-runtime capture not yet performed | 2026-08-25 | runtime actually used by the demonstration remains unpinned |
| Grasshopper | `not_recorded` | `not_recorded` | installed-runtime capture not yet performed | 2026-08-25 | runtime actually used by the demonstration remains unpinned |
| Karamba | `not_recorded` | `not_recorded` | installed-runtime capture not yet performed | 2026-08-25 | preliminary-evidence runtime remains unpinned |
| released Speckle Rhino/Grasshopper connector | `not_recorded` | `not_recorded` | installed connector capture not yet performed | 2026-08-25 | released connector and repository source must not be equated |
| current Speckle API or SDK client | `not_recorded` | `not_recorded` | client environment capture not yet performed | 2026-08-25 | released-path retrieval client is unpinned |
| accessible released Speckle service deployment when observable | `not_recorded` | `not_recorded` | no accessible deployment/version observed | 2026-08-25 | service identity is not observable in this collection |
| Python | installed runtime `3.13.5` | `Python 3.13.5` | `python --version` | 2026-08-25 | observed |
| operating system | host runtime | `Microsoft Windows NT 10.0.26200.0` | host OS-version observation | 2026-08-25 | observed |
| `speckle-sharp-sdk` | `big-truck` source pin | `f87d39cff9f54aff6c30b634780c834ba070ff4e` | approved Delta source ledger | 2026-08-24 | research source only; see `BT-OBS-001` through `BT-OBS-007` |
| `speckle-sharp-connectors` | `big-truck` source pin | `0313a89878d5d91c7b69e0492da4dd7b6c76b51d` | approved Delta source ledger | 2026-08-24 | research source only; not an installed released connector |
| `speckle-server` | `main` source pin | `51d43b91c4681a75bff8b285da7f443a4599da67` | approved Delta source ledger | 2026-08-24 | research source only; `BT-OBS-005` requires validation |
| `specklepy` | `main` source pin | `5481458ecbae39f357f247deb33cb4976000e966` | approved Delta source ledger | 2026-08-24 | research source only |
| `speckle-docs` | `main` source pin | `5d88e384b62688a9b0443ad72b13069b7b16e639` | approved Delta source ledger | 2026-08-24 | research source only |

Gate 0 cannot complete and Gate 2 cannot begin while any runtime actually used by the demonstration remains `not_recorded`. The Riff dirty tree and any installed/source mismatch that affects reproducibility are current Gate-0 blockers until explained or resolved in a dated ledger entry.

## Gate 0 — Evidence Baseline

### Dependencies

The checked-in [Big Truck Agentic Delta](docs/big-truck-agentic-delta.md), the approved design, an externally recorded approved package commit or release tag, access to the listed research source pins, and every installed runtime intended for the POC. The package cannot pin its own final commit without becoming stale.

### Work

- Verify every research-source SHA.
- Record source contradictions using the Delta precedence rule: executable code and tests at the pinned SHA, then current handoff documents, then planning documents, then interpretation or hypothesis.
- Complete the runtime ledger for every dependency used in the POC.
- Verify the current Riff ReviewMatrix, ReviewPacket, and decision semantics against the design.
- Stop on unexplained dirty source trees or an installed/source mismatch that affects reproducibility.

### Outputs

A dated source and runtime ledger, contradiction records, and an inspection note that identifies the exact Review Matrix, ReviewPacket, and decision behavior used by the POC.

### Verification

Re-run each pin command, inspect the intended installed product versions, and confirm every ledger row has a capture method and date. Reinspect Riff's ReviewMatrix export, immutable ReviewPacket content, one terminal decision per packet, and the distinction between `review_complete` and accepted status.

### Exit Criteria

All research pins and every runtime actually used are recorded; the source precedence rule has been applied to contradictions; and there is no unexplained dirty or installed/source state affecting reproducibility.

### Claims Newly Permitted

Only evidence-backed statements about the inspected pins and recorded local runtime. Existing Delta states, including `BT-OBS-001` through `BT-OBS-007`, do not advance solely because the ledger is complete.

### Stop/Go

Stop for an unknown runtime, unexplained source dirtiness, conflicting source evidence without precedence treatment, or an installed/source mismatch. Go to Gate 1 only after Gate 0 exit criteria pass.

## Gate 1 — Canonical Integration Contracts

### Dependencies

Completed Gate 0; the approved design; and the current Riff ReviewMatrix, ReviewPacket, and decision semantics verified in Gate 0.

### Work

Define transport-neutral, schema-valid fixtures and validation rules for:

- `SpeckleVersionRef` — origin, project, model, immutable version identity;
- `SpeckleEvidenceRef` — version reference plus bounded application-ID, relation, and field evidence location;
- `RookActionBinding` — Grasshopper document ID as source canvas, versioned whole-document fingerprint, stable slider instance GUID, literal `value` parameter, Speckle target and key, strict `gh_compare_and_set_value` operation, expected pre-action value, and binding provenance version;
- `agentic_change_candidate` — source version, target application ID, parameter key, `before`, `proposed_after`, complete reviewed `RookActionBinding`, unit, comparison mode, and tolerance;
- `PreflightResult` — permit/refuse decision, deterministic refusal reasons, evidence references, and the one-use authorization key on a permitted result;
- `ReviewMatrixArtifactRef` — sidecar path, SHA-256, byte length, media type, and Review Matrix schema version;
- `AgenticChangeRecord` — immutable post-attempt lineage and verified or failed outcome;
- deterministic numeric comparison — decimal input, declared unit, comparison mode, finite nonnegative tolerance, and pass/fail result.

Static authorization permits creation of the one-use permit only when:

```text
matrix schema_version == 1.0
AND review_complete == true
AND every node status == accepted
AND exactly one node contains /payload/agentic_change_candidate
AND that node's decision.action == accept
AND source_version, target_application_id, parameter_key, before, proposed_after, the complete RookActionBinding, unit, comparison mode absolute_tolerance, and tolerance are copied unchanged into the executor request
AND version A still matches source_version
AND the reviewed binding, fingerprint algorithm, and cross-field relationships are schema-valid
AND the authorization key has not been reserved or consumed
```

After permit creation and invocation, Rook evaluates these live execution guards inside the mutation:

```text
active GH_Document.DocumentID == source_canvas_id
AND canonical whole-document fingerprint == source_canvas_state_fingerprint
AND grasshopper_component_instance_id resolves to exactly one GH_NumberSlider
AND input_or_parameter_id == value
AND live value == before
```

A static failure is a preflight refusal with no `AgenticChangeRecord`. A live guard failure writes nothing, produces `outcome: failed`, and cannot be retried.

The candidate contains the complete reviewed binding. Its `source_canvas_id` must equal the Review Matrix `canvas_id` and the canonical producer-observed `GH_Document.DocumentID`; its `source_canvas_state_fingerprint` must use `rook_canonical_ghx_sha256_v1` and a lowercase hexadecimal SHA-256 produced during snapshot capture; its target, parameter key, and expected pre-action value must exactly equal the candidate fields; and its stable Grasshopper instance ID must come from actual component-instance identity rather than a label, position, list index, nickname, or role. The POC binding is restricted to `control_type: GH_NumberSlider`, `input_or_parameter_id: value`, and `allowed_rook_operation: gh_compare_and_set_value`.

`rook_canonical_ghx_sha256_v1` is SHA-256 over a Rook-owned canonical in-memory GHX serialization of the complete active document using the pinned Grasshopper runtime. Canonicalization normalizes or explicitly excludes volatile metadata and nondeterministic ordering. Repeated captures of an unchanged document must produce byte-identical canonical GHX and the same SHA-256; a no-op Grasshopper solution or recompute must also preserve both. Snapshot capture and execution-time recomputation use the same versioned Rook code path on the Grasshopper UI thread with the same pinned Rook and Grasshopper runtimes. Cosmetic state may conservatively invalidate the fingerprint; selection and viewport state absent from GHX are not execution state. Gate 1 must demonstrate both unchanged-state invariance and sensitivity to object addition/removal, wiring, persistent values, script source, and component/pin configuration. Unknown algorithms, code-path versions, capture-time thread contexts, and runtime mismatches refuse preflight. A wrong execution thread discovered only after Rook invocation performs no mutation and is a failed authorized attempt.

`gh_compare_and_set_value` is a required POC Rook addition, not an observed current capability. One UI-thread operation must accept exactly the reviewed document ID, fingerprint algorithm and SHA-256, slider `InstanceGuid`, literal parameter `value`, expected value, proposed value, and authorization key; recompute and compare the full document fingerprint; find one `GH_NumberSlider`; compare its current decimal value with `before`; and set only its value when every guard succeeds. It rejects any document state, type, ID, parameter, or expected-value mismatch and accepts no nickname, range, extra edit arrays, or alternate control type. Its receipt returns the validated identities, recomputed fingerprint, and observed before/after values. This closes the race, source-state, and identity gaps in the current `gh_snapshot` plus `gh_edit.set_values` surface. Gate 2 stops until the installed Rook runtime implements and verifies both fingerprint capture and this compare-and-set contract.

Immediately before invocation, re-read version A and refuse unless the reviewed source version and Speckle target remain the active basis. The live Grasshopper identity and `before` comparison occur inside the mutation-bound Rook operation, not as a separate snapshot check.

Derive `authorization_key` as SHA-256 over compact, key-sorted UTF-8 JSON containing exactly `review_matrix_sha256`, `authorizing_packet_id`, and `candidate_field_path`. After all preflight checks pass, atomically exclusive-create the permitted `PreflightResult` immediately before Rook invocation. The exclusive permit path is derived from `(snapshot_id, authorizing_packet_id, candidate_field_path)`, while the file stores `authorization_key` and matrix hash. This one filesystem create is the uniqueness check across concurrent re-exports with different hashes; there is no prior lookup race. Permit creation consumes one possible attempt.

Verify numeric and unit equality only when:

```text
same parameter key
AND same declared unit
AND no implicit unit conversion
AND finite, nonnegative reviewed tolerance
AND abs(decimal(observed) - decimal(authorized)) <= decimal(tolerance)
```

Refuse zero or multiple candidates, pending/corrected/rejected nodes, altered sidecar bytes, source-version mismatch, target or cross-field mismatch, missing/duplicate/malformed reviewed binding, unknown fingerprint algorithm, fingerprint/runtime mismatch, capture-time thread-context mismatch, unit mismatch, comparison mismatch, unauthorized proposed value, or consumed authorization before permit creation. These are preflight refusals and create no `AgenticChangeRecord`. After permit creation and executor invocation, a wrong Grasshopper execution thread or live document ID, whole-document fingerprint, slider GUID, control type, parameter, ambiguity, or `before` mismatch performs no mutation but produces `AgenticChangeRecord.outcome: failed` and cannot be retried.

### Outputs

Versioned transport-neutral definitions, schema-valid positive and refusal fixtures, a byte-preserving Review Matrix sidecar procedure, binding-resolution fixtures, an immutable one-use permit fixture, and an executor-request fixture copied directly from the unique candidate.

### Verification

Validate each fixture against its contract. Demonstrate preflight acceptance only for one accepted candidate and demonstrate refusal for every listed pre-permit case. Compare the executor fixture field-for-field with the authorizing payload. Using the same versioned capture/recomputation code path on the Grasshopper UI thread and the pinned runtimes, prove that repeated captures of an untouched document yield byte-identical canonical GHX and identical SHA-256 values, that a no-op solution/recompute preserves both, and that each required material mutation—object addition/removal, wiring, persistent value, script source, and component/pin configuration—changes the fingerprint. Test normalization or explicit exclusion of volatile metadata and nondeterministic ordering. Test successful compare-and-set plus live document-state, missing, stale, wrong-type, and ambiguous resolution as post-invocation failed outcomes with no mutation; test concurrent same-key and different-hash/same-candidate permit creation; and calculate deterministic comparisons from decimal textual values without conversion.

### Exit Criteria

All contracts and fixtures validate; acceptance has exactly one authorizing node and one reviewed binding; every preflight refusal prevents invocation; every mutation-bound mismatch performs no write and creates a failed post-invocation record; one reviewed authorization permits at most one possible attempt; and source version, `before`, sidecar bytes, binding, target, unit, comparison, tolerance, and proposed value cannot change between review and executor request.

### Claims Newly Permitted

The spike has a transport-neutral authorization contract and preflight policy. This permits no released-Speckle A-to-B success claim and does not change `POC-PROOF-001`.

### Stop/Go

Stop for a schema-invalid fixture, ambiguous candidate, invalid reviewed binding, mismatch, altered artifact, consumed authorization, nonfinite or negative tolerance, or any implicit unit conversion. Treat live identity or value mismatch from the invoked compare-and-set as an expected failed-outcome path, not a preflight refusal. Go to Gate 2 only after every preflight and mutation-bound case passes and the installed Rook runtime implements the reviewed-GUID, mutation-bound `gh_compare_and_set_value` contract.

## Gate 2 — Self-Sufficient Released-Speckle POC

### Dependencies

Completed Gates 0 and 1; an accessible released Speckle service or self-hosted equivalent; the released connector; the civic-canopy definition; Karamba; Riff/Chirp; the external main agent; and Rook.

### Work

Execute in this exact order:

1. Publish or identify version A with explicit stable application IDs.
2. Retrieve bounded evidence through the current Speckle object API or SDK.
3. Confirm the released Grasshopper connector exposes the same state.
4. Capture preliminary Karamba outputs as evidence, not authority.
5. Assemble and submit one immutable Riff reasoning snapshot.
6. Complete every human review.
7. Export one successful Review Matrix response as raw bytes.
8. Write, hash, read back, and verify the sidecar.
9. Copy the full reviewed candidate, including `source_version`, whole-document fingerprint, `before`, and `RookActionBinding`, into the executor request.
10. Re-read version A; verify the static source, Speckle target, binding, and fingerprint contract, then prepare the exact reviewed compare-and-set request.
11. Atomically create the one-use permitted `PreflightResult`; never reuse it after creation.
12. Invoke one allowlisted `gh_compare_and_set_value` Rook change; it atomically verifies document ID, whole-document fingerprint, stable slider GUID, literal `value`, and live `before` before writing only `proposed_after`.
13. Publish version B when execution permits.
14. Re-read B and verify version difference, target identity, and the reviewed numeric rule.
15. Write exactly one immutable AgenticChangeRecord after the executor was invoked, including the authorization key and selected binding.

### Outputs

Retained A and B version references when B is published; bounded evidence references; the raw Review Matrix sidecar and its hash/length record; one exact executor request; binding-resolution evidence; the immutable one-use permitted `PreflightResult`; action-attempt evidence; deterministic verification evidence; and exactly one immutable post-attempt outcome record.

### Verification

- A and B are distinct immutable Speckle versions when publication succeeds.
- The target application ID resolves as intended in B.
- Static authorization passed before permit creation; the Rook receipt proves the complete live canvas fingerprint and pre-action value were compared in the same operation that performed the mutation.
- The authorization key was created once and cannot be reused for a concurrent or later attempt.
- The parameter and unit match the reviewed candidate.
- Verification applies the reviewed deterministic tolerance.
- The matrix artifact hash and byte length revalidate.
- The outcome record is verified only when every check passes.
- Failure after executor invocation produces outcome: failed and preserves B when B exists.
- No claim of structural approval, production readiness, or Big Truck compatibility is made.

### Exit Criteria

The retained evidence proves the exact reviewed, uniquely authorized request was attempted once, only after live pre-action and binding checks; the independent B retrieval satisfies the reviewed rule and stable target identity; and the one post-attempt record is `verified`. If the authorization permit was created but invocation is uncertain, or if the authorized executor is invoked and any later check fails, never retry that reviewed snapshot. Retain the permit and, after invocation, the safe `failed` record and available B reference rather than infer success.

### Claims Newly Permitted

`POC-PROOF-001` may change from `poc_hypothesis` to `proven_locally` only after this gate passes with retained evidence. No result permits a structural-approval, production-readiness, or Big Truck-compatibility claim.

### Stop/Go

Stop before invocation for any Gate-1 refusal. A refusal before permit creation may be retried only while the same reviewed artifact still matches the live state; stale source, binding, or `before` data requires a new snapshot and review. Any failure or uncertainty after permit creation also requires a new snapshot and review. Stop the success path after a failed publication or verification and produce the failed post-attempt record where the executor was invoked. Go to Gate 3 only after a verified Gate-2 result; Gate 2 does not require private Speckle or unreleased Big Truck access.

## Gate 3 — Local Big Truck Parity Experiment

### Dependencies

Completed Gate 2, the five pinned Big Truck research repositories, reproducible public dependencies/toolchain, the released-path baseline evidence, and the same predefined civic-canopy evidence questions.

### Work

- Verify public dependencies before attempting bundle generation.
- Stop and record the blocker rather than recreate unavailable private schemas.
- Use the same canopy evidence questions as the released path.
- Require semantic parity before efficiency measurements.
- Report the transparent scorecard from `BT-HYP-001`: facts resolved correctly; identity and relationships preserved; bytes transferred or read; objects and geometry materialized; elapsed retrieval time; normalized evidence size; and model-input tokens.
- Use scale variants only after the real canopy and only when useful.

### Outputs

Either a dated reproducibility-blocker record or a parity dataset with question-by-question answers and direct scorecard measurements. Preserve source-pin and toolchain evidence with either outcome.

### Verification

Confirm public dependency availability before generation. Compare every local answer, identity reference, and relationship reference with its released-path counterpart before collecting or interpreting measurements. Verify that scale variants preserve deterministic evidence structure and unique stable IDs when used.

### Exit Criteria

Either complete semantic parity is retained before any efficiency conclusion, or a reproducibility blocker is recorded with the dependency, command, pin, and observed failure. Both `complete` and `blocked` are honest outcomes.

### Claims Newly Permitted

Only retained semantic-parity and direct-measurement statements for `BT-HYP-001`; no composite score, scalability conclusion, native service claim, or general identity guarantee. A blocker permits only the blocker statement. `BT-OBS-007` remains a dependency risk unless locally reproduced.

### Stop/Go

Stop for unavailable or nonreproducible public dependencies, schema gaps, or failed semantic parity; do not recreate private schemas. Go to Gate 4 only when Gate 3 names one unresolved protocol question that a narrow emulator can answer; otherwise Gate 4 stops.

## Gate 4 — Conditional Protocol Emulator

### Dependencies

Gate 3 has named one unresolved protocol question, identified the exact Delta reference it relates to, and shown that no available public path answers it. The emulator scope is limited to that one question.

### Work

Implement and exercise only the minimal local exchange needed to answer the named question; preserve inputs, expected behavior, and results; retire the emulator after the experiment or isolate it as disposable spike work.

### Outputs

A dated question statement, bounded emulator protocol fixture, local result, and explicit applicability limit tied to `PROTO-001`, `PROTO-002`, or `PROTO-003` where applicable.

### Verification

Show that the result answers the stated Gate-3 question and does not silently add discovery, identity, artifact, or service behaviors outside the fixture.

### Exit Criteria

The single question is answered or the local experiment is recorded as blocked. An emulator result is local evidence, not service compatibility.

### Claims Newly Permitted

Only local behavior of the narrowly defined emulator. It changes neither `BT-VALIDATE-001` nor any Speckle compatibility claim.

### Stop/Go

Stop when Gate 3 does not provide a focused unresolved question, when the scope grows beyond it, or when the fixture cannot answer it. Go to Gate 5 only if external validation is desired; Gate 4 is not a prerequisite for Gate 5.

## Gate 5 — Optional Speckle Validation

### Dependencies

Completed Gate 2; an optional Speckle engagement path, retained local evidence, and a bounded written request that identifies the exact claims and protocol questions to validate.

### Work

- Be optional.
- List the exact claims and protocol questions sent to Speckle.
- Request correction of inaccurate assumptions.
- Validate or revise `BT-VALIDATE-001` and `PROTO-001` through `PROTO-003`.
- Avoid the word certification unless Speckle adopts it.
- Leave Gate-2 POC completion unchanged.

### Outputs

A dated request/evidence packet, Speckle feedback or validation evidence when supplied, and explicit revisions to relevant evidence states or protocol questions.

### Verification

Cross-check each response against the exact submitted claim/question, retain corrections verbatim where appropriate, and ensure local source observations are not upgraded without supporting evidence.

### Exit Criteria

Speckle validates, corrects, or declines each submitted item, and the Delta claim state is revised only to the extent of retained feedback. Lack of engagement leaves this optional gate uncompleted without changing Gate 2.

### Claims Newly Permitted

Only the explicitly supported validation or correction statement. `BT-VALIDATE-001` and `PROTO-001` through `PROTO-003` remain validation-bound unless evidence supports a narrower revision.

### Stop/Go

Stop on no optional engagement path, incomplete question framing, or requested private material. Go only on a bounded public or authorized validation interaction; never characterize that interaction as certification unless Speckle uses that term.

## Verification Matrix

| Requirement | Gate | Evidence artifact | Pass condition | Failure behavior | Delta reference |
| --- | --- | --- | --- | --- | --- |
| stable source identity | 0 | dated source/runtime ledger and pin outputs | each research SHA and used runtime is captured; contradictions use precedence | stop on unknown pin, unexplained dirtiness, or runtime mismatch | `BT-OBS-001`–`BT-OBS-007` |
| complete accepted review | 1, 2 | raw Review Matrix sidecar | schema `1.0`, `review_complete`, and every node accepted | preflight refusal; no action and no `AgenticChangeRecord` | `POC-PROOF-001` |
| unique action candidate | 1, 2 | matrix fixture and authorizing-node record | exactly one `/payload/agentic_change_candidate` with `decision.action == accept` | preflight refusal for zero or multiple candidates | `POC-PROOF-001` |
| exact executor request | 1, 2 | candidate and executor-request fixture | source version, whole-document fingerprint, `before`, full binding, target, parameter, proposed value, unit, `absolute_tolerance`, and tolerance copied unchanged | preflight refusal | `POC-PROOF-001` |
| deterministic Rook binding | 1, 2 | `RookActionBinding` and compare-and-set receipt | reviewed document ID and stable slider `InstanceGuid` resolve to exactly one `GH_NumberSlider.value` target | invalid reviewed binding refuses preflight; live mismatch after invocation writes nothing and creates failed record | `POC-PROOF-001` |
| fresh canvas and pre-action state | 1, 2 | fingerprint capture, version-A re-read, and compare-and-set receipt | source version matches; Rook atomically requires the complete document fingerprint and live value to match before writing | invalid fingerprint contract refuses preflight; live mismatch after invocation writes nothing and creates failed record | `POC-PROOF-001` |
| one-use authorization | 1, 2 | immutable permitted `PreflightResult` | one exclusive tuple-derived permit succeeds across same-key and different-hash concurrent exports | refusal; uncertainty after permit requires new review | `POC-PROOF-001` |
| sidecar byte integrity | 1, 2 | raw UTF-8 sidecar, SHA-256, byte length | write, hash, read back, and revalidate identical bytes | preflight refusal for altered bytes | `POC-PROOF-001` |
| preflight refusal | 1 | negative fixtures and `PreflightResult` | all listed pre-permit invalid states refuse before executor invocation | preserve refusal evidence; no `AgenticChangeRecord` | `POC-PROOF-001` |
| execution failure record | 2 | immutable post-attempt record | any invoked compare-and-set identity/value failure or later failure yields `outcome: failed` | no retry; retain safe failed record and B when present | `POC-PROOF-001` |
| version-B existence | 2 | version B reference and publication evidence | B exists as a distinct immutable version when publication succeeds | failed outcome when invocation occurred and publication fails | `POC-PROOF-001` |
| independent B retrieval | 2 | retrieval transcript and bounded evidence | B is re-read rather than trusted from publication response | failed outcome after invocation | `POC-PROOF-001` |
| numeric and unit verification | 1, 2 | decimal comparison record | same key/unit, no conversion, finite nonnegative tolerance, and observed value within tolerance | refusal before action or failed outcome after action | `POC-PROOF-001` |
| released-path evidence parity | 2, 3 | predefined canopy question/answer set | released path supplies the baseline answers used in parity comparison | do not measure or claim parity | `BT-HYP-001` |
| Big Truck semantic parity | 3 | local/released answer and identity comparison | all equivalent canopy facts, identities, and relationships match | record blocker or failed parity; no efficiency conclusion | `BT-HYP-001`, `BT-OBS-002`–`BT-OBS-004` |
| efficiency measurements | 3 | direct transparent scorecard | semantic parity first; report each direct measure without composite score | withhold measurement interpretation | `BT-HYP-001` |

## Risk and Dependency Register

| Risk or dependency | Gate(s) | Mitigation / stop condition |
| --- | --- | --- |
| unreleased Big Truck drift | 0, 3, 5 | retain source pins; never silently replace a pin; seek Gate-5 correction for native seam claims |
| unavailable generated schema dependency | 3 | verify dependencies first; record blocker and do not recreate private schemas (`BT-OBS-007`) |
| released connector versus repository-main confusion | 0, 2 | capture installed released connector independently; never equate it with a source commit |
| installed/source runtime mismatch | 0, 2 | stop until installed build and source relationships are recorded |
| producer-dependent application ID stability | 2, 3 | use explicit civic-canopy IDs and verify A-to-B continuity without universalizing it (`BT-OBS-003`) |
| stale or ambiguous Speckle-to-Grasshopper binding | 1, 2 | review the complete binding and whole-document fingerprint; require the narrow Rook operation to validate canvas state and stable slider GUID atomically; stop unless every live guard matches |
| authorization replay or uncertain retry | 1, 2 | derive the exclusive permit path from snapshot/packet/candidate; store the hash-dependent key inside; require a new snapshot after uncertainty or failure |
| unit or tolerance mismatch | 1, 2 | exact copy and decimal/no-conversion preflight and verification rules |
| Riff process-local state loss before sidecar capture | 1, 2 | capture raw successful Review Matrix bytes, hash, read back, and verify before action |
| small-model measurement noise | 3 | run real canopy first; use only useful deterministic scale variants after parity |
| overclaiming professional authority | all | state that Karamba is evidence and human authorization is not engineering approval |
| protocol emulator scope growth | 4 | require one named Gate-3 question and stop for scope expansion |

## Upstream Pin and Update Policy

Upstream changes never silently replace pins. A new SHA requires a dated ledger entry, targeted reinspection of affected claims, and explicit status changes. Reinspection follows the Delta precedence rule and preserves contradictions rather than reconciling them into unsupported claims. A source update never substitutes for recording the installed runtime used by a result.

## Promotion Boundary into Riff

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

## Stop/Go Rules

| Condition | Required decision |
| --- | --- |
| Gate 0 has `not_recorded` runtime gaps, unexplained dirtiness, or reproducibility-relevant installed/source mismatch | stop; complete or explain the ledger before Gate 1 or Gate 2 begins |
| Gate 1 pre-permit authorization, reviewed-binding, replay, or schema checks fail | stop before executor invocation; retain refusal evidence and create no `AgenticChangeRecord` |
| Invoked compare-and-set rejects live document ID, whole-document fingerprint, identity, type, parameter, ambiguity, or `before` | perform no mutation; retain one immutable failed outcome and require a new snapshot/review |
| A permit exists for the authorization or reviewed candidate | do not invoke again; require a new snapshot and human review |
| Gate 2 fails after executor invocation | stop the verified-success path; retain one immutable `failed` outcome and B when present |
| Gate 3 has public-dependency or generated-schema blockers | stop and record the blocker; do not recreate unavailable private schemas |
| Gate 4 lacks one focused Gate-3 question | stop; do not build an emulator |
| Gate 5 has no optional validation path | leave it optional and preserve the Gate-2 POC state |

## Decision Log

| Date | Decision | Rationale / constraint |
| --- | --- | --- |
| 2026-08-24 | Approved two-document split | The Delta contains the technical proposition and evidence ledger; this Roadmap contains execution gates without duplicating the argument. |
| 2026-08-24 | Riff owns semantics | Riff owns reasoning, review, and decision semantics; the spike owns persistence, lineage, verification, and comparison. |
| 2026-08-24 | One unique authorizing candidate | Exactly one Review Matrix node with `/payload/agentic_change_candidate` and an accept decision can authorize the request. |
| 2026-08-24 | Outcome record is post-attempt | Preflight refusals create no `AgenticChangeRecord`; an authorized executor invocation has exactly one immutable verified or failed outcome record. |
| 2026-08-24 | Big Truck is post-POC research | Gates 3 and 4 are stoppable research; Gate 5 is optional and Gate 2 completes independently with released capabilities. |
| 2026-08-25 | Runtime baseline blocked | Riff has untracked files and several installed runtime rows are `not_recorded`; Gate 0 cannot complete and Gate 2 cannot begin. |
| 2026-08-25 | Static authorization and live guards are distinct | Static source/binding checks occur before permit creation; after invocation Rook atomically validates the complete document fingerprint, identity, and live value with mutation, and any mismatch is a failed authorized attempt. |
| 2026-08-25 | Authorization is single-use | An atomic permit consumes one possible attempt; replay, failure, or uncertainty requires a new snapshot and review. |
