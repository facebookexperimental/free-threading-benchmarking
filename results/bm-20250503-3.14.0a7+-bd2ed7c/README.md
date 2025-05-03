# Results

- fork: python/bd2ed7c7ce58084c682a
- version: 3.14.0a7+
- config: 
- commit hash: [bd2ed7c](https://github.com/python/cpython/commit/bd2ed7c)
- commit date: 2025-05-03T01:35:30+02:00
- commit merge base: [49ea8a0b2d5d65122e5e661be8a2ff9809c09cc0](https://github.com/python/cpython/commit/49ea8a0b2d5d65122e5e661be8a2ff9809c09cc0)
- ref: bd2ed7c7ce58084c682a

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14805543535)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-6.8.0-1024-aws-x86_64-with-glibc2.35
- [raw results](bm-20250503-linux-x86_64-python-bd2ed7c7ce58084c682a-3.14.0a7%2B-bd2ed7c.json)

### vs. 3.12.6

- Geometric mean: 1.190x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250503-linux-x86_64-python-bd2ed7c7ce58084c682a-3.14.0a7%2B-bd2ed7c-vs-3.12.6.md)
- [📈time plot](bm-20250503-linux-x86_64-python-bd2ed7c7ce58084c682a-3.14.0a7%2B-bd2ed7c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.145x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250503-linux-x86_64-python-bd2ed7c7ce58084c682a-3.14.0a7%2B-bd2ed7c-vs-3.13.0rc2.md)
- [📈time plot](bm-20250503-linux-x86_64-python-bd2ed7c7ce58084c682a-3.14.0a7%2B-bd2ed7c-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14805543535)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250503-vultr-x86_64-python-bd2ed7c7ce58084c682a-3.14.0a7%2B-bd2ed7c.json)

### vs. 3.12.6

- Geometric mean: 1.106x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250503-vultr-x86_64-python-bd2ed7c7ce58084c682a-3.14.0a7%2B-bd2ed7c-vs-3.12.6.md)
- [📈time plot](bm-20250503-vultr-x86_64-python-bd2ed7c7ce58084c682a-3.14.0a7%2B-bd2ed7c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.067x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250503-vultr-x86_64-python-bd2ed7c7ce58084c682a-3.14.0a7%2B-bd2ed7c-vs-3.13.0rc2.md)
- [📈time plot](bm-20250503-vultr-x86_64-python-bd2ed7c7ce58084c682a-3.14.0a7%2B-bd2ed7c-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14805543535)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7%2B-bd2ed7c.json)

### vs. 3.12.6

- Geometric mean: 1.114x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7%2B-bd2ed7c-vs-3.12.6.md)
- [📈time plot](bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7%2B-bd2ed7c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.033x faster (HPT: reliability of 94.18%, 1.00x faster at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7%2B-bd2ed7c-vs-3.13.0rc2.md)
- [📈time plot](bm-20250503-macm4pro-arm64-python-bd2ed7c7ce58084c682a-3.14.0a7%2B-bd2ed7c-vs-3.13.0rc2.svg)

