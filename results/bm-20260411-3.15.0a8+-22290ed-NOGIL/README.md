# Results

- fork: python/22290ed011a8ac406039
- version: 3.15.0a8+
- config: NOGIL
- commit hash: [22290ed](https://github.com/python/cpython/commit/22290ed)
- commit date: 2026-04-11T17:46:06-07:00
- commit merge base: [b216d7b0be725bcf0d25f3d5dade0fb06f59c71a](https://github.com/python/cpython/commit/b216d7b0be725bcf0d25f3d5dade0fb06f59c71a)
- ref: 22290ed011a8ac406039

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24295233477)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260411-macm4pro-arm64-python-22290ed011a8ac406039-3.15.0a8%2B-22290ed.json)

### vs. 3.12.6

- Geometric mean: 1.097x faster (HPT: reliability of 99.79%, 1.01x faster at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260411-macm4pro-arm64-python-22290ed011a8ac406039-3.15.0a8%2B-22290ed-vs-3.12.6.md)
- [📈time plot](bm-20260411-macm4pro-arm64-python-22290ed011a8ac406039-3.15.0a8%2B-22290ed-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.018x faster (HPT: reliability of 57.51%, 1.00x faster at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260411-macm4pro-arm64-python-22290ed011a8ac406039-3.15.0a8%2B-22290ed-vs-3.13.0rc2.md)
- [📈time plot](bm-20260411-macm4pro-arm64-python-22290ed011a8ac406039-3.15.0a8%2B-22290ed-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.056x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260411-macm4pro-arm64-python-22290ed011a8ac406039-3.15.0a8%2B-22290ed-vs-base-mem.svg)
- [📄table](bm-20260411-macm4pro-arm64-python-22290ed011a8ac406039-3.15.0a8%2B-22290ed-vs-base.md)
- [📈time plot](bm-20260411-macm4pro-arm64-python-22290ed011a8ac406039-3.15.0a8%2B-22290ed-vs-base.svg)

