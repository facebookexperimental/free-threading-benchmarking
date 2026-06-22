# Results

- fork: python/1b9fe5c7226eccc8b269
- version: 3.16.0a0
- config: JIT
- commit hash: [1b9fe5c](https://github.com/python/cpython/commit/1b9fe5c)
- commit date: 2026-06-21T01:26:53+03:00
- commit merge base: [aec0aed197872adf96d3f25fd5ea624508fcddbf](https://github.com/python/cpython/commit/aec0aed197872adf96d3f25fd5ea624508fcddbf)
- ref: 1b9fe5c7226eccc8b269

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/27888787805)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260621-vultr-x86_64-python-1b9fe5c7226eccc8b269-3.16.0a0-1b9fe5c.json)

### vs. 3.12.6

- Geometric mean: 1.171x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260621-vultr-x86_64-python-1b9fe5c7226eccc8b269-3.16.0a0-1b9fe5c-vs-3.12.6.md)
- [📈time plot](bm-20260621-vultr-x86_64-python-1b9fe5c7226eccc8b269-3.16.0a0-1b9fe5c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.131x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260621-vultr-x86_64-python-1b9fe5c7226eccc8b269-3.16.0a0-1b9fe5c-vs-3.13.0rc2.md)
- [📈time plot](bm-20260621-vultr-x86_64-python-1b9fe5c7226eccc8b269-3.16.0a0-1b9fe5c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.077x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.05x
- [🧠memory plot](bm-20260621-vultr-x86_64-python-1b9fe5c7226eccc8b269-3.16.0a0-1b9fe5c-vs-base-mem.svg)
- [📄table](bm-20260621-vultr-x86_64-python-1b9fe5c7226eccc8b269-3.16.0a0-1b9fe5c-vs-base.md)
- [📈time plot](bm-20260621-vultr-x86_64-python-1b9fe5c7226eccc8b269-3.16.0a0-1b9fe5c-vs-base.svg)

