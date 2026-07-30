# PK/ADME Pipeline Atlas

Interactive map of a 9-stage pipeline that turns regulator drug labels (EMA · MHRA · FDA · ANSM · emc)
into ML-ready pharmacokinetic / ADME data — **Acquire → Clean → Prose → Extract → Distill → Convert →
Fine-tune → Evaluate → Enrich & flatten** — built over a merged knowledge graph of the pipeline's
source repositories.

**View it live** via this repository's GitHub Pages (the link is in the repo's *About* panel / *Settings →
Pages*). Or download **`index.html`** and open it in any browser — it's fully self-contained: no server,
no build step, no network requests, everything inlined.

## What's inside

| View | What it shows |
|---|---|
| **Guided** | Step S1→S9. Each stage shows its central "god-node" script and the supporting modules around it; click any node to see what it interacts with. |
| **Diagrams** | Per-stage architecture / data-flow diagrams. |
| **Full mesh** | Every module in 3D — a prism (one facet per stage) or a globe — colored by stage, with the cross-repo hand-offs highlighted. |
| **Scoring** | The honest evaluation history: pipeline-version F1 over time, model-arm head-to-heads, per-parameter F1 (fine-tune vs stock), and category / composition / db_source breakdowns. |

**Data-honesty note.** Eval sets are kept strictly separate: synthetic regression benchmarks score
~0.84–0.96 F1, while the real hand-annotated gold scores ~0.25–0.79 — the views never mix the two, and a
cross-set delta is never presented as progress.

`WALKTHROUGH.md` is the same god-node content as a written document.

---

_This is the rendered, self-contained atlas of a private research pipeline — the interactive artifact
only; the pipeline source and build inputs are not part of this repository._
