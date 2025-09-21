# Results

- fork: python/20d5494c88985beb925b
- version: 3.15.0a0
- config: JIT
- commit hash: [20d5494](https://github.com/python/cpython/commit/20d5494)
- commit date: 2025-09-20T11:01:44+03:00
- commit merge base: [69c6b438e84ef2bb94a587e49946a2a4b6454fb3](https://github.com/python/cpython/commit/69c6b438e84ef2bb94a587e49946a2a4b6454fb3)
- ref: 20d5494c88985beb925b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17886510324)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250920-vultr-x86_64-python-20d5494c88985beb925b-3.15.0a0-20d5494.json)

### vs. 3.12.6

- Geometric mean: 1.079x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250920-vultr-x86_64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-3.12.6.md)
- [📈time plot](bm-20250920-vultr-x86_64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.043x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250920-vultr-x86_64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-3.13.0rc2.md)
- [📈time plot](bm-20250920-vultr-x86_64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.006x faster (HPT: reliability of 81.89%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250920-vultr-x86_64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-base-mem.svg)
- [📄table](bm-20250920-vultr-x86_64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-base.md)
- [📈time plot](bm-20250920-vultr-x86_64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-base.svg)

