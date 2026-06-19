# Results

- fork: python/8d7c6dcde053eec618d8
- version: 3.16.0a0
- config: NOGIL
- commit hash: [8d7c6dc](https://github.com/python/cpython/commit/8d7c6dc)
- commit date: 2026-06-18T09:08:00+09:00
- commit merge base: [a8d74c062fe3c5cb2962dde8bee83704fcfa1bc9](https://github.com/python/cpython/commit/a8d74c062fe3c5cb2962dde8bee83704fcfa1bc9)
- ref: 8d7c6dcde053eec618d8

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/27730031225)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc.json)

### vs. 3.12.6

- Geometric mean: 1.035x slower (HPT: reliability of 89.84%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc-vs-3.12.6.md)
- [📈time plot](bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.068x slower (HPT: reliability of 98.34%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc-vs-3.13.0rc2.md)
- [📈time plot](bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.102x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc-vs-base-mem.svg)
- [📄table](bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc-vs-base.md)
- [📈time plot](bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc-vs-base.svg)

