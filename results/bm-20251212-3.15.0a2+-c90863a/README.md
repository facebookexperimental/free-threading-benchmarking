# Results

- fork: python/c90863ac3dcbc5b0b8f9
- version: 3.15.0a2+
- config: 
- commit hash: [c90863a](https://github.com/python/cpython/commit/c90863a)
- commit date: 2025-12-12T21:23:18+00:00
- commit merge base: [0a97941245f1dda6d838f9aaf0512104e5253929](https://github.com/python/cpython/commit/0a97941245f1dda6d838f9aaf0512104e5253929)
- ref: c90863ac3dcbc5b0b8f9

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20183757319)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2%2B-c90863a.json)

### vs. 3.12.6

- Geometric mean: 1.075x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2%2B-c90863a-vs-3.12.6.md)
- [📈time plot](bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2%2B-c90863a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.039x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2%2B-c90863a-vs-3.13.0rc2.md)
- [📈time plot](bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2%2B-c90863a-vs-3.13.0rc2.svg)

