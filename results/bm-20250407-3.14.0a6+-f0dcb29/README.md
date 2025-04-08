# Results

- fork: python/f0dcb29d3affbbe1ec25
- version: 3.14.0a6+
- config: 
- commit hash: [f0dcb29](https://github.com/python/cpython/commit/f0dcb29)
- commit date: 2025-04-07T17:27:54+00:00
- commit merge base: [bc5233b6a5cdd8f77a4737ce317f94110869c082](https://github.com/python/cpython/commit/bc5233b6a5cdd8f77a4737ce317f94110869c082)
- ref: f0dcb29d3affbbe1ec25

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14320494922)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6%2B-f0dcb29.json)

### vs. 3.12.6

- Geometric mean: 1.077x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6%2B-f0dcb29-vs-3.12.6.md)
- [📈time plot](bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6%2B-f0dcb29-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.039x faster (HPT: reliability of 96.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6%2B-f0dcb29-vs-3.13.0rc2.md)
- [📈time plot](bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6%2B-f0dcb29-vs-3.13.0rc2.svg)

