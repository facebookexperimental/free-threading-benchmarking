# Results

- fork: python/7bb41aef4b7b8f3c3f07
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [7bb41ae](https://github.com/python/cpython/commit/7bb41ae)
- commit date: 2025-03-26T09:45:29+09:00
- commit merge base: [a26a301f8b09c1825b288fc8649f8174576361f4](https://github.com/python/cpython/commit/a26a301f8b09c1825b288fc8649f8174576361f4)
- ref: 7bb41aef4b7b8f3c3f07

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14073299256)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6%2B-7bb41ae.json)

### vs. 3.12.6

- Geometric mean: 1.044x slower (HPT: reliability of 99.99%, 1.02x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6%2B-7bb41ae-vs-3.12.6.md)
- [📈time plot](bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6%2B-7bb41ae-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6%2B-7bb41ae-vs-3.13.0rc2.md)
- [📈time plot](bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6%2B-7bb41ae-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x faster (HPT: reliability of 99.57%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6%2B-7bb41ae-vs-base-mem.svg)
- [📄table](bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6%2B-7bb41ae-vs-base.md)
- [📈time plot](bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6%2B-7bb41ae-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.111x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6%2B-7bb41ae-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6%2B-7bb41ae-vs-default_base_vs_NOGIL.svg)

