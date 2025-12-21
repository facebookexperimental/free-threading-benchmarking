# Results

- fork: python/8d2d7bb2e754f8649a68
- version: 3.15.0a3+
- config: NOGIL
- commit hash: [8d2d7bb](https://github.com/python/cpython/commit/8d2d7bb)
- commit date: 2025-12-20T23:42:06+00:00
- commit merge base: [2b4feee648b7af0ccca8dee167fdd21cfb0bd23a](https://github.com/python/cpython/commit/2b4feee648b7af0ccca8dee167fdd21cfb0bd23a)
- ref: 8d2d7bb2e754f8649a68

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20402009475)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb.json)

### vs. 3.12.6

- Geometric mean: 1.035x slower (HPT: reliability of 88.19%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-3.12.6.md)
- [📈time plot](bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.067x slower (HPT: reliability of 97.62%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-3.13.0rc2.md)
- [📈time plot](bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.106x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-base-mem.svg)
- [📄table](bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-base.md)
- [📈time plot](bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-vs-base.svg)

