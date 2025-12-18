# Results

- fork: python/8b64dd853ded593e1f0c
- version: 3.15.0a3+
- config: NOGIL
- commit hash: [8b64dd8](https://github.com/python/cpython/commit/8b64dd8)
- commit date: 2025-12-17T22:47:47+00:00
- commit merge base: [6e625f87d262f8dbdc439bc680626d10086d667d](https://github.com/python/cpython/commit/6e625f87d262f8dbdc439bc680626d10086d667d)
- ref: 8b64dd853ded593e1f0c

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20321683381)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8.json)

### vs. 3.12.6

- Geometric mean: 1.026x slower (HPT: reliability of 72.88%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-3.12.6.md)
- [📈time plot](bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.059x slower (HPT: reliability of 91.42%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-3.13.0rc2.md)
- [📈time plot](bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.098x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-base-mem.svg)
- [📄table](bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-base.md)
- [📈time plot](bm-20251217-vultr-x86_64-python-8b64dd853ded593e1f0c-3.15.0a3%2B-8b64dd8-vs-base.svg)

