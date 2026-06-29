# Results

- fork: python/46d1809ccd4bc0e1439a
- version: 3.16.0a0
- config: NOGIL
- commit hash: [46d1809](https://github.com/python/cpython/commit/46d1809)
- commit date: 2026-06-28T00:26:11+03:00
- commit merge base: [8107c53f0f9f54e71dbdc4fde8f6cda5b3ef800c](https://github.com/python/cpython/commit/8107c53f0f9f54e71dbdc4fde8f6cda5b3ef800c)
- ref: 46d1809ccd4bc0e1439a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/28306610022)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260628-vultr-x86_64-python-46d1809ccd4bc0e1439a-3.16.0a0-46d1809.json)

### vs. 3.12.6

- Geometric mean: 1.039x slower (HPT: reliability of 94.75%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260628-vultr-x86_64-python-46d1809ccd4bc0e1439a-3.16.0a0-46d1809-vs-3.12.6.md)
- [📈time plot](bm-20260628-vultr-x86_64-python-46d1809ccd4bc0e1439a-3.16.0a0-46d1809-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.072x slower (HPT: reliability of 98.53%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260628-vultr-x86_64-python-46d1809ccd4bc0e1439a-3.16.0a0-46d1809-vs-3.13.0rc2.md)
- [📈time plot](bm-20260628-vultr-x86_64-python-46d1809ccd4bc0e1439a-3.16.0a0-46d1809-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.106x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260628-vultr-x86_64-python-46d1809ccd4bc0e1439a-3.16.0a0-46d1809-vs-base-mem.svg)
- [📄table](bm-20260628-vultr-x86_64-python-46d1809ccd4bc0e1439a-3.16.0a0-46d1809-vs-base.md)
- [📈time plot](bm-20260628-vultr-x86_64-python-46d1809ccd4bc0e1439a-3.16.0a0-46d1809-vs-base.svg)

