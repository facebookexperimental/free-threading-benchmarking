# Results

- fork: python/1b7470f8cbff4bb9e58e
- version: 3.14.0a7+
- config: 
- commit hash: [1b7470f](https://github.com/python/cpython/commit/1b7470f)
- commit date: 2025-04-28T01:14:12+02:00
- commit merge base: [cd76eff26e5f700ffb715d9d096d2e28744d0594](https://github.com/python/cpython/commit/cd76eff26e5f700ffb715d9d096d2e28744d0594)
- ref: 1b7470f8cbff4bb9e58e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14697685776)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7%2B-1b7470f.json)

### vs. 3.12.6

- Geometric mean: 1.116x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7%2B-1b7470f-vs-3.12.6.md)
- [📈time plot](bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7%2B-1b7470f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.076x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7%2B-1b7470f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7%2B-1b7470f-vs-3.13.0rc2.svg)

