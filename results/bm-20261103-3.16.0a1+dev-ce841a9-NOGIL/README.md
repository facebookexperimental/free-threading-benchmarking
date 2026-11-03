# Results

- fork: python/ce841a9a02b9a28367b5
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [ce841a9](https://github.com/python/cpython/commit/ce841a9)
- commit date: 2026-11-03T18:30:48+01:00
- commit merge base: [431fdec842ae1460c8141ebdc27715d33bd1dade](https://github.com/python/cpython/commit/431fdec842ae1460c8141ebdc27715d33bd1dade)
- ref: ce841a9a02b9a28367b5

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/41690003577)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261103-vultr-x86_64-python-ce841a9a02b9a28367b5-3.16.0a1%2Bdev-ce841a9.json)

### vs. 3.12.6

- Geometric mean: 1.035x slower (HPT: reliability of 80.63%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261103-vultr-x86_64-python-ce841a9a02b9a28367b5-3.16.0a1%2Bdev-ce841a9-vs-3.12.6.md)
- [📈time plot](bm-20261103-vultr-x86_64-python-ce841a9a02b9a28367b5-3.16.0a1%2Bdev-ce841a9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.067x slower (HPT: reliability of 94.48%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261103-vultr-x86_64-python-ce841a9a02b9a28367b5-3.16.0a1%2Bdev-ce841a9-vs-3.13.0rc2.md)
- [📈time plot](bm-20261103-vultr-x86_64-python-ce841a9a02b9a28367b5-3.16.0a1%2Bdev-ce841a9-vs-3.13.0rc2.svg)

