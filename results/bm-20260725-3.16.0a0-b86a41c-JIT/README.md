# Results

- fork: python/b86a41cbf631c959d274
- version: 3.16.0a0
- config: JIT
- commit hash: [b86a41c](https://github.com/python/cpython/commit/b86a41c)
- commit date: 2026-07-25T16:42:44+02:00
- commit merge base: [587d0d11a630a893baca945383de71b07fbc854f](https://github.com/python/cpython/commit/587d0d11a630a893baca945383de71b07fbc854f)
- ref: b86a41cbf631c959d274

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/30181296997)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260725-vultr-x86_64-python-b86a41cbf631c959d274-3.16.0a0-b86a41c.json)

### vs. 3.12.6

- Geometric mean: 1.168x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260725-vultr-x86_64-python-b86a41cbf631c959d274-3.16.0a0-b86a41c-vs-3.12.6.md)
- [📈time plot](bm-20260725-vultr-x86_64-python-b86a41cbf631c959d274-3.16.0a0-b86a41c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.129x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260725-vultr-x86_64-python-b86a41cbf631c959d274-3.16.0a0-b86a41c-vs-3.13.0rc2.md)
- [📈time plot](bm-20260725-vultr-x86_64-python-b86a41cbf631c959d274-3.16.0a0-b86a41c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.083x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.05x
- [🧠memory plot](bm-20260725-vultr-x86_64-python-b86a41cbf631c959d274-3.16.0a0-b86a41c-vs-base-mem.svg)
- [📄table](bm-20260725-vultr-x86_64-python-b86a41cbf631c959d274-3.16.0a0-b86a41c-vs-base.md)
- [📈time plot](bm-20260725-vultr-x86_64-python-b86a41cbf631c959d274-3.16.0a0-b86a41c-vs-base.svg)

