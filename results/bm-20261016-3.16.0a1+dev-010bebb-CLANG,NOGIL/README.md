# Results

- fork: python/010bebbf9fd12bba1e3f
- version: 3.16.0a1+dev
- config: CLANG,NOGIL
- commit hash: [010bebb](https://github.com/python/cpython/commit/010bebb)
- commit date: 2026-10-16T20:24:12-07:00
- commit merge base: [801377967fd7bfa573c0b4c48e31b69d50c1da2f](https://github.com/python/cpython/commit/801377967fd7bfa573c0b4c48e31b69d50c1da2f)
- ref: 010bebbf9fd12bba1e3f

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39328141965)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261016-macm4pro-arm64-python-010bebbf9fd12bba1e3f-3.16.0a1%2Bdev-010bebb.json)

### vs. 3.12.6

- Geometric mean: 1.128x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261016-macm4pro-arm64-python-010bebbf9fd12bba1e3f-3.16.0a1%2Bdev-010bebb-vs-3.12.6.md)
- [📈time plot](bm-20261016-macm4pro-arm64-python-010bebbf9fd12bba1e3f-3.16.0a1%2Bdev-010bebb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.045x faster (HPT: reliability of 69.50%, 1.00x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261016-macm4pro-arm64-python-010bebbf9fd12bba1e3f-3.16.0a1%2Bdev-010bebb-vs-3.13.0rc2.md)
- [📈time plot](bm-20261016-macm4pro-arm64-python-010bebbf9fd12bba1e3f-3.16.0a1%2Bdev-010bebb-vs-3.13.0rc2.svg)

