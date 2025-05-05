# Results

- fork: python/af5799f3056b0eee61fc
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [af5799f](https://github.com/python/cpython/commit/af5799f)
- commit date: 2025-05-04T15:21:56-07:00
- commit merge base: [3109c47be8fc00df999c5bff01229a6b93513224](https://github.com/python/cpython/commit/3109c47be8fc00df999c5bff01229a6b93513224)
- ref: af5799f3056b0eee61fc

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14826513592)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250504-vultr-x86_64-python-af5799f3056b0eee61fc-3.14.0a7%2B-af5799f.json)

### vs. 3.12.6

- Geometric mean: 1.015x faster (HPT: reliability of 83.80%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250504-vultr-x86_64-python-af5799f3056b0eee61fc-3.14.0a7%2B-af5799f-vs-3.12.6.md)
- [📈time plot](bm-20250504-vultr-x86_64-python-af5799f3056b0eee61fc-3.14.0a7%2B-af5799f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.017x slower (HPT: reliability of 96.16%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250504-vultr-x86_64-python-af5799f3056b0eee61fc-3.14.0a7%2B-af5799f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250504-vultr-x86_64-python-af5799f3056b0eee61fc-3.14.0a7%2B-af5799f-vs-3.13.0rc2.svg)

