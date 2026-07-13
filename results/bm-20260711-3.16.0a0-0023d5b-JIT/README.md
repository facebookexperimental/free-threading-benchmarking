# Results

- fork: python/0023d5b23df09f18425f
- version: 3.16.0a0
- config: JIT
- commit hash: [0023d5b](https://github.com/python/cpython/commit/0023d5b)
- commit date: 2026-07-11T21:55:02+00:00
- commit merge base: [bbd1f2f9e0354f91c5d3c4eb3eb53657265dcc77](https://github.com/python/cpython/commit/bbd1f2f9e0354f91c5d3c4eb3eb53657265dcc77)
- ref: 0023d5b23df09f18425f

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/29173779243)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260711-vultr-x86_64-python-0023d5b23df09f18425f-3.16.0a0-0023d5b.json)

### vs. 3.12.6

- Geometric mean: 1.167x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260711-vultr-x86_64-python-0023d5b23df09f18425f-3.16.0a0-0023d5b-vs-3.12.6.md)
- [📈time plot](bm-20260711-vultr-x86_64-python-0023d5b23df09f18425f-3.16.0a0-0023d5b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.128x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260711-vultr-x86_64-python-0023d5b23df09f18425f-3.16.0a0-0023d5b-vs-3.13.0rc2.md)
- [📈time plot](bm-20260711-vultr-x86_64-python-0023d5b23df09f18425f-3.16.0a0-0023d5b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.081x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.05x
- [🧠memory plot](bm-20260711-vultr-x86_64-python-0023d5b23df09f18425f-3.16.0a0-0023d5b-vs-base-mem.svg)
- [📄table](bm-20260711-vultr-x86_64-python-0023d5b23df09f18425f-3.16.0a0-0023d5b-vs-base.md)
- [📈time plot](bm-20260711-vultr-x86_64-python-0023d5b23df09f18425f-3.16.0a0-0023d5b-vs-base.svg)

