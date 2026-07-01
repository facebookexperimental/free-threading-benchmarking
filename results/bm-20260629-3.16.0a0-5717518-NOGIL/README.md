# Results

- fork: python/5717518fb3ed6f347166
- version: 3.16.0a0
- config: NOGIL
- commit hash: [5717518](https://github.com/python/cpython/commit/5717518)
- commit date: 2026-06-29T17:05:02-07:00
- commit merge base: [2dd6e59aea24220975cce2b602846d997413d46c](https://github.com/python/cpython/commit/2dd6e59aea24220975cce2b602846d997413d46c)
- ref: 5717518fb3ed6f347166

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/28413031206)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260629-vultr-x86_64-python-5717518fb3ed6f347166-3.16.0a0-5717518.json)

### vs. 3.12.6

- Geometric mean: 1.037x slower (HPT: reliability of 93.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260629-vultr-x86_64-python-5717518fb3ed6f347166-3.16.0a0-5717518-vs-3.12.6.md)
- [📈time plot](bm-20260629-vultr-x86_64-python-5717518fb3ed6f347166-3.16.0a0-5717518-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.070x slower (HPT: reliability of 99.14%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260629-vultr-x86_64-python-5717518fb3ed6f347166-3.16.0a0-5717518-vs-3.13.0rc2.md)
- [📈time plot](bm-20260629-vultr-x86_64-python-5717518fb3ed6f347166-3.16.0a0-5717518-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.106x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260629-vultr-x86_64-python-5717518fb3ed6f347166-3.16.0a0-5717518-vs-base-mem.svg)
- [📄table](bm-20260629-vultr-x86_64-python-5717518fb3ed6f347166-3.16.0a0-5717518-vs-base.md)
- [📈time plot](bm-20260629-vultr-x86_64-python-5717518fb3ed6f347166-3.16.0a0-5717518-vs-base.svg)

