# Results

- fork: python/e42bda9441119c7952ad
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [e42bda9](https://github.com/python/cpython/commit/e42bda9)
- commit date: 2025-04-17T12:04:42+02:00
- commit merge base: [15c75d7a8b86d9f76982f70a00b69b403458694f](https://github.com/python/cpython/commit/15c75d7a8b86d9f76982f70a00b69b403458694f)
- ref: e42bda9441119c7952ad

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14523227913)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250417-vultr-x86_64-python-e42bda9441119c7952ad-3.14.0a7%2B-e42bda9.json)

### vs. 3.12.6

- Geometric mean: 1.026x faster (HPT: reliability of 66.15%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250417-vultr-x86_64-python-e42bda9441119c7952ad-3.14.0a7%2B-e42bda9-vs-3.12.6.md)
- [📈time plot](bm-20250417-vultr-x86_64-python-e42bda9441119c7952ad-3.14.0a7%2B-e42bda9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.007x slower (HPT: reliability of 90.15%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250417-vultr-x86_64-python-e42bda9441119c7952ad-3.14.0a7%2B-e42bda9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250417-vultr-x86_64-python-e42bda9441119c7952ad-3.14.0a7%2B-e42bda9-vs-3.13.0rc2.svg)

