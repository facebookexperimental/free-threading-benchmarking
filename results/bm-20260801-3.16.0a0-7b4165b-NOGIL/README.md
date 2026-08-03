# Results

- fork: python/7b4165b3b07638d8aeab
- version: 3.16.0a0
- config: NOGIL
- commit hash: [7b4165b](https://github.com/python/cpython/commit/7b4165b)
- commit date: 2026-08-01T21:54:04+02:00
- commit merge base: [7ce7f0bd8511410bf7c42cc5fc88dfafe07874b6](https://github.com/python/cpython/commit/7ce7f0bd8511410bf7c42cc5fc88dfafe07874b6)
- ref: 7b4165b3b07638d8aeab

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/30725327310)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260801-vultr-x86_64-python-7b4165b3b07638d8aeab-3.16.0a0-7b4165b.json)

### vs. 3.12.6

- Geometric mean: 1.043x slower (HPT: reliability of 93.34%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260801-vultr-x86_64-python-7b4165b3b07638d8aeab-3.16.0a0-7b4165b-vs-3.12.6.md)
- [📈time plot](bm-20260801-vultr-x86_64-python-7b4165b3b07638d8aeab-3.16.0a0-7b4165b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x slower (HPT: reliability of 99.49%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260801-vultr-x86_64-python-7b4165b3b07638d8aeab-3.16.0a0-7b4165b-vs-3.13.0rc2.md)
- [📈time plot](bm-20260801-vultr-x86_64-python-7b4165b3b07638d8aeab-3.16.0a0-7b4165b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.107x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20260801-vultr-x86_64-python-7b4165b3b07638d8aeab-3.16.0a0-7b4165b-vs-base-mem.svg)
- [📄table](bm-20260801-vultr-x86_64-python-7b4165b3b07638d8aeab-3.16.0a0-7b4165b-vs-base.md)
- [📈time plot](bm-20260801-vultr-x86_64-python-7b4165b3b07638d8aeab-3.16.0a0-7b4165b-vs-base.svg)

