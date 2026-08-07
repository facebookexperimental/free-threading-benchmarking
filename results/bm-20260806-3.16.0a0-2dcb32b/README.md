# Results

- fork: python/2dcb32b5f384d393970d
- version: 3.16.0a0
- config: 
- commit hash: [2dcb32b](https://github.com/python/cpython/commit/2dcb32b)
- commit date: 2026-08-06T08:29:22+08:00
- commit merge base: [e12ee02a164c87865b78f6d5a511f6009871383b](https://github.com/python/cpython/commit/e12ee02a164c87865b78f6d5a511f6009871383b)
- ref: 2dcb32b5f384d393970d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/31060260525)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260806-vultr-x86_64-python-2dcb32b5f384d393970d-3.16.0a0-2dcb32b.json)

### vs. 3.12.6

- Geometric mean: 1.067x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260806-vultr-x86_64-python-2dcb32b5f384d393970d-3.16.0a0-2dcb32b-vs-3.12.6.md)
- [📈time plot](bm-20260806-vultr-x86_64-python-2dcb32b5f384d393970d-3.16.0a0-2dcb32b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.032x faster (HPT: reliability of 99.85%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260806-vultr-x86_64-python-2dcb32b5f384d393970d-3.16.0a0-2dcb32b-vs-3.13.0rc2.md)
- [📈time plot](bm-20260806-vultr-x86_64-python-2dcb32b5f384d393970d-3.16.0a0-2dcb32b-vs-3.13.0rc2.svg)

