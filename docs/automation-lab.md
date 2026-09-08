# AI and automation: four product workstreams

[Repository overview](../README.md) · [Requirements library](portfolio.md)

Automation changes the shape of work: someone must still know what started, what finished, what needs review and what failed. These projects extend the portfolio beyond trading interfaces into content operations, AI-assisted review and local-AI discovery.

## Content operations

**Evidence:** content configuration, daily-news, generated-content and storyline artifacts were identified. Workbook metadata also shows organization around content preparation, sources, formats and run history. This establishes a structured workspace; it does not establish audience reach, successful publication or time saved.

**Product problem:** content preparation spans source selection, drafting, format adaptation and review. Without visible workflow ownership, an output can be mistaken for a finished publishing task.

**Proposed product extension:** a reviewable editorial queue that separates prepared material from approved material and delivery status.

| Stage | User question | Proposed behavior |
| --- | --- | --- |
| Intake | What is this work based on? | Keep source provenance available to the reviewer |
| Preparation | Is this a draft or ready for review? | Make generation and editing status explicit |
| Review | Which version am I approving? | Associate the review decision with a specific version |
| Delivery | Did the requested delivery complete? | Keep acknowledgment distinct from confirmation |
| Recovery | What can I safely resume? | Preserve completed work and identify failed work |

**Scope decision:** start with a review queue and traceable draft versions. Multi-channel publishing should follow only after ownership and delivery feedback are defined. A generated draft alone is not evidence of completed publication.

**Synthetic acceptance:** revise a draft after review. The changed version must return to review rather than inherit an earlier decision silently. Simulate a delivery failure; the completed draft remains available while delivery stays visibly unresolved.

**Success evidence to collect:** time spent locating the correct version, review rework, unresolved delivery attempts and provenance gaps. Baselines and measured outcomes are not yet claimed.

## Social-message preparation

**Evidence:** a dedicated social-message workbook exists alongside the wider content artifacts. Delivery integrations and published outcomes were not verified.

**Product problem:** adapting a shared idea to different destinations can create inconsistent versions and duplicate effort.

**Proposed scope:** one preparation task with clearly identified destination variants, separate review state for each variant and a visible relationship to its source draft. Actual account details and publishing configuration are excluded.

**Trade-off:** reusing a shared draft reduces repetition, but changes to it can invalidate previously prepared variants. The product should surface that dependency for review.

**Acceptance example:** update the source draft in a synthetic task. A reviewer can identify which variants were prepared from the earlier version. No automated send is part of the public example.

## AI-assisted review workflow

**Evidence:** local review-orchestration and background-work artifacts exist. The public case focuses on task lifecycle and human review; private prompts, analytical material and generated findings are excluded.

**Product problem:** a generated response can arrive late, fail, or be mistaken for an authoritative decision. It must remain attached to the right task and clearly distinguish generated material from a human disposition.

**Proposed user journey:** request review → observe pending work → inspect generated material → record human review → retain the task's disposition.

**Scope decision:** make asynchronous ownership and review status dependable before expanding model choice or automating downstream action.

| Failure scenario | Proposed acceptance behavior |
| --- | --- |
| Response arrives after navigation | It remains attached to the originating task |
| Generation fails | Failure is visible; silence is not completion |
| Output is incomplete | The reviewer sees incompleteness before recording a disposition |
| A task is revised | Earlier output cannot silently become the result for the new version |
| Review is still pending | Generated material is not presented as a verified finding |

These criteria are a new public specification. They do not claim model evaluation scores or prove deployed behavior.

## Local-AI exploration

**Evidence:** a localized language-model environment is recorded as a project exploration. A working local deployment, hardware benchmark or production adoption has not been established.

**Discovery question:** which bounded tasks could benefit from a locally operated model, given setup effort, responsiveness, output quality and ongoing maintenance?

**Proposed experiment:** select a non-sensitive task using entirely synthetic material. Compare whether the output satisfies a task-specific rubric, how often review is required, the observed response time and the effort required to operate the environment. Establish evaluation criteria before choosing a model.

**Decision gate:** proceed only if the task-level evidence warrants the operating burden. Retain human review while exploring suitability. Local operation alone does not establish output quality or fitness for a workflow.

## Shared product lesson

Automation value depends on the handoffs: provenance, version identity, review, delivery and recovery. Those responsibilities are concrete enough to specify and test even when generation and implementation remain private.

---

© Justin Joseph. Portfolio documentation. Production implementation and proprietary methods are not included.
