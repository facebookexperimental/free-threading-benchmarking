# Results

- fork: python/0ec3aee262b03276a18a
- version: 3.16.0a0
- config: 
- commit hash: [0ec3aee](https://github.com/python/cpython/commit/0ec3aee)
- commit date: 2026-10-09T22:25:44Z
- commit merge base: [5a22a62b96a68c2dd31784c5e3427ad7b365388a](https://github.com/python/cpython/commit/5a22a62b96a68c2dd31784c5e3427ad7b365388a)
- ref: 0ec3aee262b03276a18a

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/38010408728)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee.json)

### vs. 3.12.6

- Geometric mean: 1.161x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.12.6.md)
- [📈time plot](bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.072x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.13.0rc2.md)
- [📈time plot](bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.13.0rc2.svg)

