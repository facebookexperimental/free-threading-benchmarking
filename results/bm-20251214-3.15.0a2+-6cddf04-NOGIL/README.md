# Results

- fork: python/6cddf04344a1e8ca9df5
- version: 3.15.0a2+
- config: NOGIL
- commit hash: [6cddf04](https://github.com/python/cpython/commit/6cddf04)
- commit date: 2025-12-14T01:03:23+02:00
- commit merge base: [e5a48480c0eb64d5af11f33658c2a3f1170e4ddd](https://github.com/python/cpython/commit/e5a48480c0eb64d5af11f33658c2a3f1170e4ddd)
- ref: 6cddf04344a1e8ca9df5

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20199900240)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2%2B-6cddf04.json)

### vs. 3.12.6

- Geometric mean: 1.034x slower (HPT: reliability of 84.08%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2%2B-6cddf04-vs-3.12.6.md)
- [📈time plot](bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2%2B-6cddf04-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.067x slower (HPT: reliability of 93.82%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2%2B-6cddf04-vs-3.13.0rc2.md)
- [📈time plot](bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2%2B-6cddf04-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.107x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2%2B-6cddf04-vs-base-mem.svg)
- [📄table](bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2%2B-6cddf04-vs-base.md)
- [📈time plot](bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2%2B-6cddf04-vs-base.svg)

