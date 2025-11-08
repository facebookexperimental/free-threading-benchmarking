# Results

- fork: python/d13ee0ae186f4704f3b6
- version: 3.15.0a1+
- config: 
- commit hash: [d13ee0a](https://github.com/python/cpython/commit/d13ee0a)
- commit date: 2025-11-07T13:46:47-05:00
- commit merge base: [3989e12d39bfe2587e5ba80873c37e0c2d449088](https://github.com/python/cpython/commit/3989e12d39bfe2587e5ba80873c37e0c2d449088)
- ref: d13ee0ae186f4704f3b6

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19184932946)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1%2B-d13ee0a.json)

### vs. 3.12.6

- Geometric mean: 1.134x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1%2B-d13ee0a-vs-3.12.6.md)
- [📈time plot](bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1%2B-d13ee0a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.052x faster (HPT: reliability of 99.92%, 1.00x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1%2B-d13ee0a-vs-3.13.0rc2.md)
- [📈time plot](bm-20251107-macm4pro-arm64-python-d13ee0ae186f4704f3b6-3.15.0a1%2B-d13ee0a-vs-3.13.0rc2.svg)

