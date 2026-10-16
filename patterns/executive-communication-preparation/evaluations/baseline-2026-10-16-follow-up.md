# Follow-Up Behavioral Evaluation — 2026-10-16

## Run Metadata

| Field | Recorded value |
|---|---|
| Scope | Readiness precedence, complete effective profiles, and site/action ownership scope |
| Date | October 16, 2026; America/Lima; invocation timestamps retained in UTC |
| Parent | [First baseline](baseline-2026-10-16.md) and its [run packet](runs/2026-10-16.json), preserved byte-for-byte |
| Instruction revision | 2026-10-16 follow-up 1; frozen SHA-256 `826ace43e22c7d7002acd85c4f0ade1671faa1474fa3e8ea3463a30899b137ae` |
| Runtime | codex-cli 0.162.0-alpha.17.2; requested `gpt-6.1-sol`, reasoning `high`, preserving configured user defaults |
| Cases | Nine byte-identical baseline inputs and three separately identified changed-fixture controls; all inputs, expectations, and instructions frozen before generation |
| Method | One fresh ephemeral invocation per input, sequentially; no expected answers, prior outputs, review keys, or drafting conversation intentionally supplied |
| Review | First-party, model-assisted and expectation-aware; no independent human review |
| Artifacts | [Follow-up run packet](runs/2026-10-16-follow-up.json): instruction text, exact inputs, raw response text, hashes, invocation metadata, comparisons, and per-dimension findings |

## Changes Evaluated

- Readiness now distinguishes the primary label from separate information-blocker and human-review lists. An unsuitable-channel requirement takes precedence; otherwise missing/disputed required information precedes pending approval. Ready for sender review requires neither a blocker nor additional approval.
- A current profile must include all active inherited rules. An unavailable inheritance reference blocks readiness even when case evidence is otherwise sufficient; a complete inlined current profile does not require an older file.
- Owner scope remains limited to the supported site, service, action, and phase. The model must not expand first-site fallback ownership or update coverage to a newly affected site, including in recipient-facing copy.

The frozen revised instructions were not tuned during this batch. Current fictional examples and the profile template were updated as documentation companions; only the frozen instructions and individual inputs were intentionally supplied to subjects.

## Results

All 12 responses matched the frozen primary-readiness expectations and met the targeted substantive checks in this first-party review. No clear critical failure was identified. This is a targeted smoke result, not validation of the whole pattern or repeated reliability.

| Case | Input comparison | Prior actual readiness | Follow-up actual readiness | Targeted checks |
|---|---|---|---|---|
| `replay-evidence-dispute` | Same input | Human review required | Needs information | Met |
| `replay-handoff-missing-leader-direction` | Same input | Human review required | Needs information | Met |
| `replay-learning-adopted-missing-scope` | Same input | Needs information | Needs information | Met |
| `replay-learning-adopted-complete` | Same input | Ready for sender review | Needs information | Met |
| `replay-learning-full-profile-supplement` | Same input | Ready for sender review | Ready for sender review | Met |
| `replay-changed-material-impact` | Same input | Human review required | Needs information | Met |
| `replay-legitimate-compression` | Same input | Needs information | Needs information | Met |
| `replay-legitimate-compression-complete-supplement` | Same input | Ready for sender review | Ready for sender review | Met |
| `replay-delegation-asserted-only` | Same input | Needs information | Needs information | Met |
| `framing-conflict-complete` | Changed fixture | Human review required | Human review required | Met |
| `reserved-review-complete` | Changed fixture | Human review required | Human review required | Met |
| `wider-impact-confirmed-owners` | Changed fixture | Human review required | Human review required | Met |

For changed fixtures, the prior label is context for the source case, not a controlled before/after result. Exact additions and source-case mappings are retained. Only the nine same-input rows compare the supplied input unchanged under revised instructions; they are still single observations.

### Readiness and Pending Reviews Are Separate

The disputed-evidence and missing-leader-direction replays now use Needs information and explicitly retain the pending human reviews. The wider-impact replay also uses Needs information while keeping the mandatory return to the director separate. The legitimate-compression fixture with missing update information still stops appropriately; its complete-input replay remains Ready for sender review.

The complete framing-conflict control has no information blocker but still requires truthful-framing resolution. Its actual response uses Human review required with “None for an accurate review draft” under blocking information. The complete reserved-review control likewise retains director review. These controls distinguish gathering missing information from satisfying an already established approval route.

### Missing Inheritance Blocks; Complete Guidance Does Not

Both partial-profile replays request the missing inherited requirements. In the previously qualified complete-evidence case, the follow-up explicitly says: “The supplied v2 references inherited v1 requirements but does not include them.” It uses Needs information even though scope-check ownership and timing are already supplied.

The unchanged full-profile control accepts the complete inlined current guidance, reports no blocker, and reaches Ready for sender review. It does not demand an old v1 file. The revised learning example and profile template now supply or require the full effective version rather than a runtime dependency on a previous version.

### Ownership Wording Is Bounded in the Draft Itself

The unchanged wider-impact replay now says: “The Operations lead owns fallback for the original warehouse.” It then explicitly states that second-site fallback/recovery ownership is unconfirmed and that coverage of the second site in the next update requires confirmation. The original baseline's broad fallback-ownership wording is not repeated.

The changed-fixture ownership control supplies separate second-site recovery ownership, both-site update coverage, and fresh review-only direction. The response separately assigns original-site fallback to the Operations lead and second-site recovery coordination to the second warehouse manager, using the supplied confirmation for update coverage. It keeps director review rather than reusing direct-send permission.

## Limitations

- One response per case, one requested alias/runtime, and first-party grading by the authoring assistant. There is no independent or blinded human review, statistical reliability claim, immutable backend snapshot, or complete regression of the initial suite.
- Nine inputs are unchanged; three controls change facts/direction as well as using the revised instructions. Changed-fixture outcomes cannot isolate an instruction effect. Fixtures and prior outcomes were known to the author; they are targeted regression checks, not held-out generalization evidence.
- Fresh sessions reduce conversation carryover, but platform/harness instructions and metadata may remain. Shell, search, and apps were disabled; no model tool calls were observed. No real identity, source authentication, persistence, access control, sending, or platform adapter was tested.
- The hierarchy's alternative-channel branch, genuine multi-turn pressure, independently corrected evidence sequences, real recipient feedback, and repeated-run behavior were not evaluated here.
- These observations do not validate the historical private implementation, quantify productivity, or replace the separate comparative usefulness study. Committees, presentations, and implementations remain outside this work.

## Integrity and Follow-Up

The first baseline Markdown and JSON packet, all Decision-Ready Escalations files, and existing implementation files were compared with pre-edit SHA-256 values and remain unchanged. The follow-up packet preserves every response from this batch rather than replacing first-baseline evidence.

Further confidence would require repeated fresh runs and independent human review of the scoped ownership and readiness decisions. Any further behavioral revision should receive another instruction snapshot and record. No additional trial or deployment is implied by this report.
