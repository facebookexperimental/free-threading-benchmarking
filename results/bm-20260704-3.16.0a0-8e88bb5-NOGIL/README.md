# Results

- fork: python/8e88bb56337a771f3af5
- version: 3.16.0a0
- config: NOGIL
- commit hash: [8e88bb5](https://github.com/python/cpython/commit/8e88bb5)
- commit date: 2026-07-04T19:39:11-04:00
- commit merge base: [8e580b068500feec5d6cc5e5a3e6072e8996fb25](https://github.com/python/cpython/commit/8e580b068500feec5d6cc5e5a3e6072e8996fb25)
- ref: 8e88bb56337a771f3af5

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/28724504800)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260704-vultr-x86_64-python-8e88bb56337a771f3af5-3.16.0a0-8e88bb5.json)

### vs. 3.12.6

- Geometric mean: 1.035x slower (HPT: reliability of 93.66%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260704-vultr-x86_64-python-8e88bb56337a771f3af5-3.16.0a0-8e88bb5-vs-3.12.6.md)
- [📈time plot](bm-20260704-vultr-x86_64-python-8e88bb56337a771f3af5-3.16.0a0-8e88bb5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.068x slower (HPT: reliability of 98.23%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260704-vultr-x86_64-python-8e88bb56337a771f3af5-3.16.0a0-8e88bb5-vs-3.13.0rc2.md)
- [📈time plot](bm-20260704-vultr-x86_64-python-8e88bb56337a771f3af5-3.16.0a0-8e88bb5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.106x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260704-vultr-x86_64-python-8e88bb56337a771f3af5-3.16.0a0-8e88bb5-vs-base-mem.svg)
- [📄table](bm-20260704-vultr-x86_64-python-8e88bb56337a771f3af5-3.16.0a0-8e88bb5-vs-base.md)
- [📈time plot](bm-20260704-vultr-x86_64-python-8e88bb56337a771f3af5-3.16.0a0-8e88bb5-vs-base.svg)

