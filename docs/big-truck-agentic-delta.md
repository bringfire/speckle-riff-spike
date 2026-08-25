# Big Truck Agentic Delta

> **Status:** Independent integration research observed at pinned upstream revisions on 2026-08-24. This is not a Speckle specification, compatibility claim, or product commitment.

## Executive Proposition

Speckle supplies durable, versioned project evidence. Riff supplies inspectable reasoning and consequential human authority. This spike tests whether they can be joined into a verified, auditable agent-action loop without making Riff a geometry store or treating human review as professional engineering approval.

The proposition is not that Big Truck supplies reasoning. Big Truck may make version-scoped identity, properties, topology, and selectively readable evidence substantially more useful to agents. Chirp interprets evidence, Riff exposes and records reasoning and authority, and the external agent acts only through a bounded executor after authorization.

```text
Speckle / Big Truck  → project evidence and version plane
Karamba              → preliminary deterministic analysis
Chirp                → structured interpretation and proposal
Riff                 → inspectable reasoning and human decision semantics
External main agent  → orchestration
Rook                 → one allowlisted Grasshopper action
Spike                → durable capture, lineage, verification, and comparison
```

The delta under study is not machine readability appearing from nothing. Current Speckle is machine-readable. `BT-HYP-001` is the hypothesis that purpose-separated, bounded, columnar, version-scoped consumption with explicit topology can make equivalent agent evidence questions more inspectable and less geometry-dependent.

## Independent Project Disclaimer

This is an independent, unofficial integration research project. It is not authored, endorsed, or certified by Speckle. Observations describe pinned public source revisions and may not represent the released or eventual Big Truck product. No private specification, credential, licensed binary, staging detail, or proprietary example is reproduced here.

## The Demonstration

The self-sufficient proof of concept uses released Speckle capabilities for a civic-canopy architectural study. Karamba provides preliminary deterministic evidence; it does not approve structural work or direct the change. Chirp interprets the bounded evidence and proposes one exact candidate. A human may authorize that architectural exploration, but that decision is not professional engineering approval.

```text
Speckle version A
→ bounded evidence and preliminary Karamba results
→ Chirp interpretation and one exact agentic_change_candidate
→ Riff presentation and per-node human review
→ all nodes accepted and exactly one authorizing candidate
→ raw Review Matrix response written, hashed, read back, and verified
→ source version, live before-state, and one reviewed RookActionBinding revalidated
→ one-use authorization reserved
→ external agent coordinates one allowlisted Rook action through that binding
→ Speckle version B is published
→ B is independently re-read and verified
→ one immutable AgenticChangeRecord binds the lineage
```

The executor cannot select or alter the candidate. It copies the reviewed `source_version`, target application ID, parameter key, `before`, proposed value, complete `RookActionBinding`, unit, comparison mode, and tolerance exactly. Immediately before invoking Rook it re-reads version A. The sole POC mutation is a narrow `gh_compare_and_set_value` operation that, on the Grasshopper UI thread, validates the reviewed document ID and stable slider `InstanceGuid`, compares the current value with `before`, and changes only the slider value when equal. This is a required Rook addition, not a capability claimed for the currently inspected runtime. Numeric verification evaluates the re-read result using the reviewed unit, comparison mode, and tolerance; a unit mismatch is refused or recorded as a failed outcome, never implicitly converted. The POC permits one allowlisted architectural parameter change, such as canopy bay spacing; it excludes structural member sizing, autonomous optimization, and unrestricted Grasshopper modification.

## What the Released-Speckle POC Proves

`POC-PROOF-001` is initially a `poc_hypothesis`: the released-Speckle A-to-B authority loop is not `proven_locally` until Gate 2 retains passing evidence. No POC behavior is `proven_locally` before Gate 2 passes. Gate 2 evidence must show the exact authorization, one bounded action, distinct version B, independent re-read, and deterministic verification.

Authorization and failure semantics are deliberate:

- A failed authorization or sidecar preflight performs no action and creates no AgenticChangeRecord.
- Failure after the authorized executor is invoked creates outcome: failed.
- A failed verification can retain result_version B when B was published.
- Review Matrix review_complete is necessary but insufficient; every node must be accepted.
- Exactly one node may contain payload.agentic_change_candidate.
- A missing, malformed, duplicate, or cross-field-mismatched reviewed binding is a preflight refusal.
- A stale Speckle source version is a preflight refusal.
- A live document, slider GUID, control type, parameter, or `before` mismatch discovered by the invoked compare-and-set performs no mutation but is an immutable failed authorized attempt.
- A one-use authorization permit is atomically reserved immediately before the Rook call; a consumed permit is never replayed.
- Failure or uncertainty after permit creation requires a new reasoning snapshot and human review.
- Riff annotations, including change_candidate, are advisory and non-executable.
- JSON sidecars are POC packaging, not the proposed permanent Big Truck representation.

The sidecar is the raw UTF-8 Review Matrix response: it is written unchanged, SHA-256 hashed with byte length, read back, and verified before execution. The spike retains refusal evidence for failed preflight but creates no immutable outcome record until an authorized executor has been invoked. A permitted `PreflightResult` acts as the one-use authorization receipt: its hash-dependent `authorization_key` binds the sidecar, authorizing packet, and candidate path, while its atomically exclusive path is derived from the snapshot, authorizing packet, and candidate path. Concurrent re-exports therefore contend for the same permit even when `exported_at` produces different matrix hashes.

## Big Truck Evidence Ledger

Evidence states used in this document:

```text
observed_upstream             directly supported by a pinned public upstream source
proven_locally                supported by a retained local artifact and repeatable verification
poc_hypothesis                a claim with a named local experiment that has not yet passed
requires_speckle_validation   a claim that cannot be resolved from public local evidence
```

| Claim ID | Evidence state | Claim or observation | Repository / branch / SHA | Source | Contradiction or limitation |
| --- | --- | --- | --- | --- | --- |
| BT-OBS-001 | observed_upstream | The pinned SDK handoff describes a 12-file Zstd Parquet bundle split across geometry, EAV, and envelope tables. | `speckle-sharp-sdk` / `big-truck` / `f87d39cff9f54aff6c30b634780c834ba070ff4e` | [notes/handoff-packfileloader2-envelope.md](https://github.com/specklesystems/speckle-sharp-sdk/blob/f87d39cff9f54aff6c30b634780c834ba070ff4e/notes/handoff-packfileloader2-envelope.md) | This is a pinned public handoff, not a released product specification. |
| BT-OBS-002 | observed_upstream | The pinned model separates object, geometry, and node namespaces and uses typed relations to connect them. | `speckle-sharp-sdk` / `big-truck` / `f87d39cff9f54aff6c30b634780c834ba070ff4e` | [notes/handoff-packfileloader2-envelope.md](https://github.com/specklesystems/speckle-sharp-sdk/blob/f87d39cff9f54aff6c30b634780c834ba070ff4e/notes/handoff-packfileloader2-envelope.md) | Namespace interpretation depends on relation type; topology is not complete AEC semantics. |
| BT-OBS-003 | observed_upstream | application_id is an addressing key, but cross-version continuity remains producer-dependent. | `speckle-sharp-sdk` / `big-truck` / `f87d39cff9f54aff6c30b634780c834ba070ff4e` | [notes/handoff-packfileloader2-envelope.md](https://github.com/specklesystems/speckle-sharp-sdk/blob/f87d39cff9f54aff6c30b634780c834ba070ff4e/notes/handoff-packfileloader2-envelope.md) | The handoff describes an object-to-application_id dictionary, not a universal continuity guarantee. |
| BT-OBS-004 | observed_upstream | The pinned bundle stores geometry separately from EAV and envelope/topology artifacts. | `speckle-sharp-sdk` / `big-truck` / `f87d39cff9f54aff6c30b634780c834ba070ff4e` | [notes/handoff-packfileloader2-envelope.md](https://github.com/specklesystems/speckle-sharp-sdk/blob/f87d39cff9f54aff6c30b634780c834ba070ff4e/notes/handoff-packfileloader2-envelope.md) | Separation alone does not prove every evidence question avoids geometry reads. |
| BT-OBS-005 | observed_upstream | The handoff describes a version-artifacts endpoint, while the pinned public server main does not independently prove that endpoint is available. | `speckle-sharp-sdk` / `big-truck` / `f87d39cff9f54aff6c30b634780c834ba070ff4e`; `speckle-server` / `main` / `51d43b91c4681a75bff8b285da7f443a4599da67` | [SDK endpoint handoff](https://github.com/specklesystems/speckle-sharp-sdk/blob/f87d39cff9f54aff6c30b634780c834ba070ff4e/notes/handoff-packfileloader2-envelope.md); [pinned server downloader](https://github.com/specklesystems/speckle-server/blob/51d43b91c4681a75bff8b285da7f443a4599da67/packages/objectloader2/src/core/stages/serverDownloader.ts) | A handoff is not independent server availability evidence; validation is required. |
| BT-OBS-006 | observed_upstream | The public Big Truck branches contain evolving artifact send/receive or exploration work and internally superseded planning material. | `speckle-sharp-connectors` / `big-truck` / `0313a89878d5d91c7b69e0492da4dd7b6c76b51d`; `speckle-sharp-sdk` / `big-truck` / `f87d39cff9f54aff6c30b634780c834ba070ff4e` | [artifact send component](https://github.com/specklesystems/speckle-sharp-connectors/blob/0313a89878d5d91c7b69e0492da4dd7b6c76b51d/Connectors/Rhino/Speckle.Connectors.GrasshopperShared/Components/Operations/Send/SendArtefactComponent.cs); [superseded endpoint handoff](https://github.com/specklesystems/speckle-sharp-sdk/blob/f87d39cff9f54aff6c30b634780c834ba070ff4e/notes/handoff-server-v2-data-endpoints.md) | Planning documents explicitly retain superseded material; executable code/tests take precedence. |
| BT-OBS-007 | observed_upstream | Reproducible local generation may remain blocked by unavailable generated speckle-bundle-spec dependencies and the required .NET toolchain version. | `speckle-sharp-sdk` / `big-truck` / `f87d39cff9f54aff6c30b634780c834ba070ff4e` | [Speckle.Sdk.Parquet.csproj](https://github.com/specklesystems/speckle-sharp-sdk/blob/f87d39cff9f54aff6c30b634780c834ba070ff4e/src/Speckle.Sdk.Parquet/Speckle.Sdk.Parquet.csproj); [global.json](https://github.com/specklesystems/speckle-sharp-sdk/blob/f87d39cff9f54aff6c30b634780c834ba070ff4e/global.json) | This identifies a public dependency risk; it does not establish licensing as the sole blocker. |
| POC-PROOF-001 | poc_hypothesis | The released-Speckle A-to-B authority loop is a poc_hypothesis until Gate 2 retains passing evidence; only then may its state become proven_locally. | Local spike / Gate 2 | [approved design §12](superpowers/specs/2026-08-24-speckle-riff-spike-document-design.md#12-roadmap-proof-gates) | No POC behavior is proven_locally before Gate 2 passes. |
| BT-HYP-001 | poc_hypothesis | Separate and selective property/topology artifacts can enable geometry-independent evidence questions and reduce transferred bytes, geometry materialization, and normalized agent context for equivalent answers. | Local spike / Gate 3 | [pinned bundle handoff](https://github.com/specklesystems/speckle-sharp-sdk/blob/f87d39cff9f54aff6c30b634780c834ba070ff4e/notes/handoff-packfileloader2-envelope.md) | Correctness parity and measured results are required; no scalability conclusion follows automatically. |
| BT-VALIDATE-001 | requires_speckle_validation | Native compatibility with Speckle's unreleased service requires Speckle validation. | Speckle validation / Gate 5 | [approved design §12](superpowers/specs/2026-08-24-speckle-riff-spike-document-design.md#12-roadmap-proof-gates) | Public local sources cannot prove interoperability with unreleased infrastructure. |

The ledger is deliberately conservative. Source precedence is executable code and tests at the pinned SHA, then current handoff documents, then planning documents, then this document's interpretation or hypothesis. Contradictions and superseded notes remain visible rather than being reconciled into a product claim.

## Big Truck's Potential Agentic Delta

| Capability | Released-path baseline | Observed Big Truck direction | Agentic consequence | Current evidence state | Proof required |
| --- | --- | --- | --- | --- | --- |
| version-scoped evidence | Current Speckle object API or SDK retrieves the evidence for a version. | `BT-OBS-001` records version-named bundle files; `BT-OBS-005` records the handoff's version-artifacts route and its unvalidated server availability. | A proposal can bind evidence questions to one source version. | observed_upstream | Gate 3 reads the pinned artifact shape; Gate 5 validates native service compatibility. |
| object addressing and producer identity | A POC producer supplies explicit application IDs and verifies A-to-B continuity. | `BT-OBS-003` records the EAV object_index-to-application_id dictionary. | The action target can be named without using geometry as identity. | observed_upstream | Gate 2 tests the producer invariant; it must not be generalized. |
| typed properties | Object API or SDK exposes current object properties. | The [pinned handoff](https://github.com/specklesystems/speckle-sharp-sdk/blob/f87d39cff9f54aff6c30b634780c834ba070ff4e/notes/handoff-packfileloader2-envelope.md) describes EAV paths, typed scalar columns, and type-scoped rows; `BT-OBS-001` records its 12-file bundle context. | Agents can ask a bounded property question with an explicit field path. | observed_upstream | Gate 3 answers predefined questions with semantic parity. |
| topology and relationships | Relationships are obtained through the released path as needed. | `BT-OBS-002` records typed envelope relations and node namespaces. | Agents can ground a question in explicit relations rather than inferred nesting alone. | observed_upstream | Gate 3 verifies relation interpretation for the canopy questions. |
| geometry-independent reads | Released path is instrumented for the same evidence questions. | `BT-OBS-004` records separate geometry, EAV, and envelope artifacts. | `BT-HYP-001`: some equivalent questions may omit geometry materialization. | poc_hypothesis | Compare semantic parity, bytes, and materialization for equivalent questions. |
| columnar and bounded consumption | Baseline instrumentation records object/API retrieval. | `BT-OBS-001` records Parquet files; the [pinned handoff](https://github.com/specklesystems/speckle-sharp-sdk/blob/f87d39cff9f54aff6c30b634780c834ba070ff4e/notes/handoff-packfileloader2-envelope.md) describes independently useful table sets. | `BT-HYP-001`: consumers may read only the evidence categories a question needs. | poc_hypothesis | Gate 3 measures bytes and normalized evidence after correctness passes. |
| artifact reuse between agents | Each agent can receive spike-owned evidence references. | `BT-OBS-005` records a handoff-described artifact route but not a proven discovery contract. | A shared bounded reference could prevent repeated extraction. | requires_speckle_validation | Validate discovery, schema, and access semantics with Speckle. |
| cross-version comparison when identity is stable | POC verifies producer-supplied application ID continuity. | `BT-OBS-003` records application_id addressing, not a universal continuity contract. | `BT-HYP-001`: stable IDs may support an exact A-to-B comparison. | poc_hypothesis | Gate 2 proves this only for the civic-canopy producer. |

## Canonical Evidence and Action Lineage

The spike's canonical seam is the immutable `AgenticChangeRecord` described in the [approved specification](superpowers/specs/2026-08-24-speckle-riff-spike-document-design.md#8-agenticchangerecord), not a new Speckle or Riff schema. Its semantic layers are:

```text
source evidence
→ exact authorization artifact and action candidate
→ attempted action
→ result version when published
→ deterministic verification
→ verified or failed outcome
```

It binds source version A, grounded evidence, the exact hashed Review Matrix sidecar, the uniquely authorizing Riff packet and candidate field, the one-use authorization key, the reviewed `RookActionBinding`, the one Rook attempt, result version B when published, and re-read verification. Publishing B alone never means success. Once the authorized executor is invoked, execution, publication, or verification failure is recorded immutably with `outcome: failed`; safe failure contains no credentials, private exceptions, prompts, or stack traces.

## Identity Guarantees and Limits

The spike keeps `canvas_id`, `snapshot_id`, `run_id`, `node_id`/component ID, `packet_id`, Speckle application ID, and Speckle version ID separate. The civic-canopy producer supplies explicit application IDs and Gate 2 verifies their continuity from A to B. That is a POC invariant, not a claim that Big Truck or Speckle universally guarantees cross-version identity.

`BT-OBS-003` supports application_id as an addressing key in the pinned handoff. It does not support an identity guarantee across producers, versions, imports, remaps, or future product revisions.

The reviewed `RookActionBinding` is a separate POC invariant. It records the producer-observed Grasshopper `GH_Document.DocumentID` as source `canvas_id`, stable slider `InstanceGuid`, literal `value` parameter, Speckle target application ID and parameter key, `gh_compare_and_set_value`, expected pre-action value, and binding provenance version. The mutation itself must resolve that stable identity to exactly one `GH_NumberSlider` and compare the live value before writing. Current Rook snapshots expose only routing short IDs and component-type GUIDs, so they are not accepted as durable identity proof; inability to perform the stable-ID compare-and-set stops the POC rather than permitting a label-, position-, or index-based guess.

## Responsibility and Authority Boundaries

Speckle/Big Truck provides project evidence and the version plane. Karamba supplies preliminary deterministic analysis. Chirp supplies structured interpretation and proposal. Riff supplies inspectable reasoning and human decision semantics. The external main agent orchestrates; Rook performs one allowlisted Grasshopper action; the spike owns durable capture, lineage, verification, and comparison.

Riff priority is not a human decision, an accepted review is not engineering approval, and a proposed agent action is not execution. No actor in this POC replaces deterministic calculation, professional engineering judgment, or licensed approval.

## Temporary-to-Native Replacement Map

| Layer | Current boundary | Replacement rule |
| --- | --- | --- |
| Temporary released path | Current Speckle object API or SDK plus released Grasshopper connector sanity check | Use to complete Gate 2 without private or unreleased access. |
| Durable spike contract | Evidence references, authorization policy, sidecar digest, AgenticChangeRecord, deterministic verification | Preserve across transports; these are the research seam. |
| Potential native path | Big Truck artifact discovery and bounded evidence consumption after validation | Adopt only after Gates 3 and 5 establish the required behavior. |
| Disposable work | Transport-specific adapters and any local protocol emulator | Remove or isolate; an emulator never proves production compatibility. |

## Measurement Strategy

Comparison is correctness first. The released-path baseline and the Big Truck experiment must answer the same predefined civic-canopy evidence questions before efficiency measurements are interpreted. The transparent scorecard is:

```text
facts resolved correctly
identity and relationships preserved
bytes transferred or read
objects and geometry materialized
elapsed retrieval time
normalized evidence size
model-input tokens
```

The real civic canopy is primary. One or two deterministic scale variants are permitted only if the real model is too small to reveal an interpretable difference. Results report each measure directly: there is no composite score and no extrapolation to production performance.

## Protocol Opportunities

These are bounded questions for Speckle, not requirements or inferred backlog. An opportunity is retired if evidence shows Big Truck already solves it or the POC does not need it.

### PROTO-001 — identity continuity metadata

| Field | Entry |
| --- | --- |
| opportunity_id | PROTO-001 |
| problem_observed | `BT-OBS-003` provides an addressing key but does not establish how a producer created it or whether continuity is expected across versions. |
| agentic_benefit | A verifier could distinguish a producer-declared continuity invariant from an inferred match. |
| upstream_evidence | `BT-OBS-003`; [pinned EAV identity dictionary](https://github.com/specklesystems/speckle-sharp-sdk/blob/f87d39cff9f54aff6c30b634780c834ba070ff4e/notes/handoff-packfileloader2-envelope.md). |
| current_limitation | The spike can test only its own producer-supplied IDs. |
| candidate_protocol_capability | Question for Speckle: could producers declare how an application ID was established and whether it is expected to persist across versions? |
| compatibility_concern | It must not reinterpret historical IDs or create a universal identity promise. |
| validation_needed | Speckle validation and a cross-version producer test. |
| status | requires_speckle_validation |

### PROTO-002 — grounded derived-evidence references

| Field | Entry |
| --- | --- |
| opportunity_id | PROTO-002 |
| problem_observed | The spike needs to bind Karamba and Chirp-derived claims to exact source version, application ID, relation, and field-level evidence. |
| agentic_benefit | A reviewer and verifier can re-ground a proposal without treating Riff as a geometry store. |
| upstream_evidence | `BT-OBS-001`, `BT-OBS-002`, and `BT-OBS-004` describe separable tables, identity, and typed relations. |
| current_limitation | The spike owns evidence references and sidecar packaging; no native Big Truck convention is established here. |
| candidate_protocol_capability | Question for Speckle: could derived analysis artifacts cite source version, application ID, relationship, and field-level evidence through a stable convention? |
| compatibility_concern | It must remain optional, avoid embedding private reasoning, and preserve version-specific interpretation. |
| validation_needed | Gate 3 parity evidence and Speckle validation. |
| status | requires_speckle_validation |

### PROTO-003 — artifact capability discovery

| Field | Entry |
| --- | --- |
| opportunity_id | PROTO-003 |
| problem_observed | A bounded consumer must know which schemas, relation types, and evidence categories exist without private or out-of-band knowledge. |
| agentic_benefit | Agents can request and validate only the evidence categories a question needs. |
| upstream_evidence | `BT-OBS-001`, `BT-OBS-002`, and the pinned handoff's catalog and artifact-route description. |
| current_limitation | `BT-OBS-005` does not independently prove endpoint availability in pinned public server main. |
| candidate_protocol_capability | Question for Speckle: could consumers discover which schemas, relation types, and evidence categories a bundle contains without private or out-of-band knowledge? |
| compatibility_concern | Discovery must tolerate optional files and evolving schemas rather than hardcoding a private contract. |
| validation_needed | Inspect executable endpoint/service behavior with Speckle. |
| status | requires_speckle_validation |

## Permitted and Prohibited Claims

### Permitted claims

At the pinned revisions, the public sources support the seven `BT-OBS-*` observations under their stated limitations. The POC is allowed to claim a verified A-to-B authority loop only after Gate 2 retains its local artifacts and passes deterministic verification. The potential benefits in `BT-HYP-001` remain hypotheses until semantic parity and measurements are retained. Native service compatibility remains `BT-VALIDATE-001`.

### Prohibited claims

This document must not claim:

- Big Truck is a final or stable public specification.
- Big Truck universally guarantees cross-version identity.
- The public branches are independently buildable today.
- Selective artifacts automatically make agents scalable.
- The envelope represents complete AEC semantics.
- Riff reasoning is already a Speckle primitive.
- Human authorization is engineering approval.
- The protocol emulator proves production compatibility.
- Licensing is the sole access or build blocker.

## Questions for Speckle

- For `BT-VALIDATE-001`, what public validation path can establish whether this spike's bounded artifact consumption is compatible with the unreleased service, without relying on private material?
- For `PROTO-001`, can producers declare application-ID provenance and intended cross-version continuity without turning that declaration into a universal guarantee?
- For `PROTO-002`, is there an appropriate stable convention for a derived evidence reference to cite version, application ID, relation, and field path?
- For `PROTO-003`, can a consumer discover available schemas, relation types, and evidence categories from a bundle or service contract without out-of-band schema knowledge?

## Source Notes

Observations were made on 2026-08-24 against these pins: `speckle-sharp-sdk` `big-truck` `f87d39cff9f54aff6c30b634780c834ba070ff4e`; `speckle-sharp-connectors` `big-truck` `0313a89878d5d91c7b69e0492da4dd7b6c76b51d`; `speckle-server` `main` `51d43b91c4681a75bff8b285da7f443a4599da67`; `specklepy` `main` `5481458ecbae39f357f247deb33cb4976000e966`; and `speckle-docs` `main` `5d88e384b62688a9b0443ad72b13069b7b16e639`.

Source precedence is executable code and tests at the pinned SHA, then current handoff documents, then planning documents, then local interpretation. The public SDK project references generated files from a sibling `speckle-bundle-spec` checkout, which is a known public-dependency and toolchain reproducibility blocker for local generation. This document requests no private specification, credentials, licensed binary, staging detail, or proprietary example.
