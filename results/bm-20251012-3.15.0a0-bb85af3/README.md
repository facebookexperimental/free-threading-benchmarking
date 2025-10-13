# Results

- fork: python/bb85af343f331b104e3b
- version: 3.15.0a0
- config: 
- commit hash: [bb85af3](https://github.com/python/cpython/commit/bb85af3)
- commit date: 2025-10-12T15:17:41-07:00
- commit merge base: [5f91d5d9a4187c4bfa2ddd653b819b12eb3ad477](https://github.com/python/cpython/commit/5f91d5d9a4187c4bfa2ddd653b819b12eb3ad477)
- ref: bb85af343f331b104e3b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18451712627)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251012-vultr-x86_64-python-bb85af343f331b104e3b-3.15.0a0-bb85af3.json)

### vs. 3.12.6

- Geometric mean: 1.074x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251012-vultr-x86_64-python-bb85af343f331b104e3b-3.15.0a0-bb85af3-vs-3.12.6.md)
- [📈time plot](bm-20251012-vultr-x86_64-python-bb85af343f331b104e3b-3.15.0a0-bb85af3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.038x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251012-vultr-x86_64-python-bb85af343f331b104e3b-3.15.0a0-bb85af3-vs-3.13.0rc2.md)
- [📈time plot](bm-20251012-vultr-x86_64-python-bb85af343f331b104e3b-3.15.0a0-bb85af3-vs-3.13.0rc2.svg)

