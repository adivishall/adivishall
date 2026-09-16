## Adi Vishal

CS undergraduate at VIT Pune. I write systems-flavoured code, hand-built data
structures in C++, computer-vision pipelines in Python and care more about the
engineering around a model than the model itself.

What I'm trying to get good at is **measurement**: benchmarks that report where a
fast structure *loses*, evaluations that separate what was proven from what was
assumed, and claims scoped to the evidence behind them.

**Languages** &nbsp;C++ · Python<br>
**Focus** &nbsp;Data structures & algorithms · Applied ML / computer vision · LLM-agent security

[LinkedIn](https://www.linkedin.com/in/adivishal) · [Email](mailto:adi.vishal.21052006@gmail.com)

---

### Projects

**[Sentinel](https://github.com/adivishall/sentinel)** &nbsp;·&nbsp; Python

An AI firewall for LLM agents that make irreversible decisions. The verdict is a
pure function of verified ledger facts, never attacker-controlled prose the trust
boundary is a type (`UntrustedText` vs `TrustedFacts`) checked by mypy. Evaluated
offline against a simulated agent; the README says so up front.

**[SafeTrail](https://github.com/adivishall/safetrail)** &nbsp;·&nbsp; C++17, no dependencies

A geofencing engine with every spatial index written by hand instead of delegated
to PostGIS, quadtree, R-tree, AVL interval tree, a persistent path-copying
quadtree, rollback union-find. All validated against a brute-force oracle (0
mismatches across 18,000 queries), with a benchmark that reports its own crossover
points.

**[Two-Wheeler Safety](https://github.com/adivishall/two-wheeler-safety)** &nbsp;·&nbsp; Python, YOLOv8, Flask

Traffic-violation detection where the hard part is everything after the detector:
Hungarian plate-to-rider assignment, crossframe OCR voting, temporal violation
confirmation. Detector baseline mAP@50 0.697; system-level numbers are synthetic
and demonstrate the pipeline is correct, not that it's accurate in the field.

---

### Currently

Working through algorithms seriously, and looking for the thing I keep missing:
code review from engineers who didn't write the code.
