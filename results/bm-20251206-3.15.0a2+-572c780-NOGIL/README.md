# Results

- fork: python/572c780aa875e4eb0096
- version: 3.15.0a2+
- config: NOGIL
- commit hash: [572c780](https://github.com/python/cpython/commit/572c780)
- commit date: 2025-12-06T22:37:34+00:00
- commit merge base: [332da6295f365b09cabf30a9222323b056ab1410](https://github.com/python/cpython/commit/332da6295f365b09cabf30a9222323b056ab1410)
- ref: 572c780aa875e4eb0096

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19996253276)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780.json)

### vs. 3.12.6

- Geometric mean: 1.037x slower (HPT: reliability of 88.47%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-3.12.6.md)
- [📈time plot](bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.070x slower (HPT: reliability of 98.99%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-3.13.0rc2.md)
- [📈time plot](bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.109x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-base-mem.svg)
- [📄table](bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-base.md)
- [📈time plot](bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-base.svg)

