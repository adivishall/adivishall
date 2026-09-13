## Adi Vishal

CSE undergraduate at VIT Pune. I mostly write systems-flavoured code: hand-built
data structures in C++, computer-vision pipelines in Python, and the engineering
around a model rather than the model itself.

What I'm actually trying to get good at is **measurement** — benchmarks that
report where a fast structure *loses*, evaluations that separate what was proven
from what was assumed, and claims scoped to the evidence behind them.

---

### Projects

**[safetrail](https://github.com/adivishall/safetrail)** · C++17, no dependencies

A geofencing engine where the spatial indexes are written by hand rather than
delegated to PostGIS: quadtree, R-tree, AVL interval tree, a persistent
path-copying quadtree for historical queries, and union-find with rollback. Every
index is validated against a brute-force oracle — 285 assertions across 28 test
files, 0 mismatches across 18,000 queries.

The benchmark is the part I'd point at first. It reports the crossover points
(the k-d tree *loses* to a linear scan below ~64 nodes), measures 10.1× structural
sharing in the persistent quadtree, and includes an analysis of why the index
speedup ceilings at ~33× instead of the ~29,000× a naive reading of the
complexity would predict — it's output-bound, not search-bound.

Course project on simulated tourists over real OpenStreetMap geography. Not a product.

**[two-wheeler-safety](https://github.com/adivishall/two-wheeler-safety)** · Python, YOLOv8, Flask

Traffic-violation detection where the hard part is everything after the detector.
Plate-to-rider attribution is a matching problem solved with Hungarian assignment
over a geometric cost; OCR is stabilised by cross-frame voting plus structural
plate validation; violations must persist across frames before they're recorded;
speed comes from video time (`frame/fps`), never wall-clock.

Detector baseline is mAP@50 0.697 on an imbalanced dataset. The system-level
numbers are from synthetic scenarios and demonstrate the pipeline is correct, not
that it's accurate in the field — the README keeps those two claims apart on purpose.

**[sentinel](https://github.com/adivishall/sentinel)** · Python

An argument that LLM agents making irreversible decisions shouldn't compute those
decisions from attacker-controlled text. The verdict is a pure function of the
bank's own ledger fields; the customer's prose only selects *which* verified fact
to check. The boundary is a type (`UntrustedText` vs `TrustedFacts`), checked by
mypy and pinned by tests.

Evaluated offline against a simulated agent, so the headline numbers demonstrate
the design rather than measure a real model — the README says so up front, and
notes that of four layers, exactly one does the blocking.

---

### Currently

Working through algorithms seriously, and looking for the thing I keep missing:
code review from engineers who didn't write the code.

Reachable at adi.vishal.21052006@gmail.com.
