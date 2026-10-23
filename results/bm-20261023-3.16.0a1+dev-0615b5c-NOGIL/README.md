# Results

- fork: python/0615b5c0d9ee3854bc50
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [0615b5c](https://github.com/python/cpython/commit/0615b5c)
- commit date: 2026-10-23T17:20:53+00:00
- commit merge base: [74c91a6fbfa3625cdc850acc99b509cc3d8c6ed0](https://github.com/python/cpython/commit/74c91a6fbfa3625cdc850acc99b509cc3d8c6ed0)
- ref: 0615b5c0d9ee3854bc50

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/40000440133)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261023-vultr-x86_64-python-0615b5c0d9ee3854bc50-3.16.0a1%2Bdev-0615b5c.json)

### vs. 3.12.6

- Geometric mean: 1.039x slower (HPT: reliability of 75.64%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261023-vultr-x86_64-python-0615b5c0d9ee3854bc50-3.16.0a1%2Bdev-0615b5c-vs-3.12.6.md)
- [📈time plot](bm-20261023-vultr-x86_64-python-0615b5c0d9ee3854bc50-3.16.0a1%2Bdev-0615b5c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.071x slower (HPT: reliability of 98.36%, 1.00x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261023-vultr-x86_64-python-0615b5c0d9ee3854bc50-3.16.0a1%2Bdev-0615b5c-vs-3.13.0rc2.md)
- [📈time plot](bm-20261023-vultr-x86_64-python-0615b5c0d9ee3854bc50-3.16.0a1%2Bdev-0615b5c-vs-3.13.0rc2.svg)

