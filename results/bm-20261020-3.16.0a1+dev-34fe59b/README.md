# Results

- fork: python/34fe59b878335856ddfe
- version: 3.16.0a1+dev
- config: 
- commit hash: [34fe59b](https://github.com/python/cpython/commit/34fe59b)
- commit date: 2026-10-20T02:32:08+02:00
- commit merge base: [fa8600cb1dd2ad33e95d3cfbed55208e35f5b472](https://github.com/python/cpython/commit/fa8600cb1dd2ad33e95d3cfbed55208e35f5b472)
- ref: 34fe59b878335856ddfe

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39348925828)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261020-macm4pro-arm64-python-34fe59b878335856ddfe-3.16.0a1%2Bdev-34fe59b.json)

### vs. 3.12.6

- Geometric mean: 1.205x faster (HPT: reliability of 100.00%, 1.11x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261020-macm4pro-arm64-python-34fe59b878335856ddfe-3.16.0a1%2Bdev-34fe59b-vs-3.12.6.md)
- [📈time plot](bm-20261020-macm4pro-arm64-python-34fe59b878335856ddfe-3.16.0a1%2Bdev-34fe59b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.114x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261020-macm4pro-arm64-python-34fe59b878335856ddfe-3.16.0a1%2Bdev-34fe59b-vs-3.13.0rc2.md)
- [📈time plot](bm-20261020-macm4pro-arm64-python-34fe59b878335856ddfe-3.16.0a1%2Bdev-34fe59b-vs-3.13.0rc2.svg)

