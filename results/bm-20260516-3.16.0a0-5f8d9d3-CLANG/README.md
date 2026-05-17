# Results

- fork: python/5f8d9d35753e22946880
- version: 3.16.0a0
- config: CLANG
- commit hash: [5f8d9d3](https://github.com/python/cpython/commit/5f8d9d3)
- commit date: 2026-05-16T11:24:41-07:00
- commit merge base: [a7ed0c9e1dee1397e80e2e0d90d110155da2bc30](https://github.com/python/cpython/commit/a7ed0c9e1dee1397e80e2e0d90d110155da2bc30)
- ref: 5f8d9d35753e22946880

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25977025233)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260516-vultr-x86_64-python-5f8d9d35753e22946880-3.16.0a0-5f8d9d3.json)

### vs. 3.12.6

- Geometric mean: 1.095x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: 2to3, aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260516-vultr-x86_64-python-5f8d9d35753e22946880-3.16.0a0-5f8d9d3-vs-3.12.6.md)
- [📈time plot](bm-20260516-vultr-x86_64-python-5f8d9d35753e22946880-3.16.0a0-5f8d9d3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: 2to3, aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260516-vultr-x86_64-python-5f8d9d35753e22946880-3.16.0a0-5f8d9d3-vs-3.13.0rc2.md)
- [📈time plot](bm-20260516-vultr-x86_64-python-5f8d9d35753e22946880-3.16.0a0-5f8d9d3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.026x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.02x
- [🧠memory plot](bm-20260516-vultr-x86_64-python-5f8d9d35753e22946880-3.16.0a0-5f8d9d3-vs-base-mem.svg)
- [📄table](bm-20260516-vultr-x86_64-python-5f8d9d35753e22946880-3.16.0a0-5f8d9d3-vs-base.md)
- [📈time plot](bm-20260516-vultr-x86_64-python-5f8d9d35753e22946880-3.16.0a0-5f8d9d3-vs-base.svg)

