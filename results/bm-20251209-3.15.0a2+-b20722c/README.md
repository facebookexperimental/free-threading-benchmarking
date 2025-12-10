# Results

- fork: python/b20722c300a78c384620
- version: 3.15.0a2+
- config: 
- commit hash: [b20722c](https://github.com/python/cpython/commit/b20722c)
- commit date: 2025-12-09T17:03:13+01:00
- commit merge base: [1b460fcddc420ce791f7f7bb33b260826034f3c9](https://github.com/python/cpython/commit/1b460fcddc420ce791f7f7bb33b260826034f3c9)
- ref: b20722c300a78c384620

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20072673836)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2%2B-b20722c.json)

### vs. 3.12.6

- Geometric mean: 1.073x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2%2B-b20722c-vs-3.12.6.md)
- [📈time plot](bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2%2B-b20722c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.038x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2%2B-b20722c-vs-3.13.0rc2.md)
- [📈time plot](bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2%2B-b20722c-vs-3.13.0rc2.svg)

