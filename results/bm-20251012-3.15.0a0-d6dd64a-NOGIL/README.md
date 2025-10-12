# Results

- fork: python/d6dd64ac654898b4ce71
- version: 3.15.0a0
- config: NOGIL
- commit hash: [d6dd64a](https://github.com/python/cpython/commit/d6dd64a)
- commit date: 2025-10-12T01:52:01+03:00
- commit merge base: [35e9d41a9cc3999672ba7440847b16ec71bd9ddd](https://github.com/python/cpython/commit/35e9d41a9cc3999672ba7440847b16ec71bd9ddd)
- ref: d6dd64ac654898b4ce71

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18436503023)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a.json)

### vs. 3.12.6

- Geometric mean: 1.015x slower (HPT: reliability of 79.94%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-3.12.6.md)
- [📈time plot](bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.049x slower (HPT: reliability of 94.05%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-3.13.0rc2.md)
- [📈time plot](bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.092x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-base-mem.svg)
- [📄table](bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-base.md)
- [📈time plot](bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-base.svg)

