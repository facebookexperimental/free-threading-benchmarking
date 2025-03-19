# Results

- fork: python/f81990024554a75e2ab3
- version: 3.14.0a6+
- config: CLANG,NOGIL
- commit hash: [f819900](https://github.com/python/cpython/commit/f819900)
- commit date: 2025-03-18T17:34:01+01:00
- commit merge base: [49234c065cf2b1ea32c5a3976d834b1d07b9b831](https://github.com/python/cpython/commit/49234c065cf2b1ea32c5a3976d834b1d07b9b831)
- ref: f81990024554a75e2ab3

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13934588318)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250318-vultr-x86_64-python-f81990024554a75e2ab3-3.14.0a6%2B-f819900.json)

### vs. 3.12.6

- Geometric mean: 1.046x faster (HPT: reliability of 64.51%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250318-vultr-x86_64-python-f81990024554a75e2ab3-3.14.0a6%2B-f819900-vs-3.12.6.md)
- [📈time plot](bm-20250318-vultr-x86_64-python-f81990024554a75e2ab3-3.14.0a6%2B-f819900-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.013x faster (HPT: reliability of 84.42%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250318-vultr-x86_64-python-f81990024554a75e2ab3-3.14.0a6%2B-f819900-vs-3.13.0rc2.md)
- [📈time plot](bm-20250318-vultr-x86_64-python-f81990024554a75e2ab3-3.14.0a6%2B-f819900-vs-3.13.0rc2.svg)

