# Results

- fork: python/95e5d596308620acbd86
- version: 3.15.0a1+
- config: NOGIL
- commit hash: [95e5d59](https://github.com/python/cpython/commit/95e5d59)
- commit date: 2025-10-24T20:02:17+05:30
- commit merge base: [ebf99384966344df77828e69dd88d34df878a7b6](https://github.com/python/cpython/commit/ebf99384966344df77828e69dd88d34df878a7b6)
- ref: 95e5d596308620acbd86

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18784042880)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1%2B-95e5d59.json)

### vs. 3.12.6

- Geometric mean: 1.076x faster (HPT: reliability of 94.39%, 1.00x faster at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1%2B-95e5d59-vs-3.12.6.md)
- [📈time plot](bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1%2B-95e5d59-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.002x slower (HPT: reliability of 74.92%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1%2B-95e5d59-vs-3.13.0rc2.md)
- [📈time plot](bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1%2B-95e5d59-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.006x slower (HPT: reliability of 96.33%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1%2B-95e5d59-vs-base-mem.svg)
- [📄table](bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1%2B-95e5d59-vs-base.md)
- [📈time plot](bm-20251024-macm4pro-arm64-python-95e5d596308620acbd86-3.15.0a1%2B-95e5d59-vs-base.svg)

