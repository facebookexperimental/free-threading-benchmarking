# Results

- fork: python/8a00c9a4d2ce9d373b13
- version: 3.14.0a6+
- config: 
- commit hash: [8a00c9a](https://github.com/python/cpython/commit/8a00c9a)
- commit date: 2025-03-27T21:06:52+02:00
- commit merge base: [972a295fe34280aa3d16c573d6200025a1ce4ff0](https://github.com/python/cpython/commit/972a295fe34280aa3d16c573d6200025a1ce4ff0)
- ref: 8a00c9a4d2ce9d373b13

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14119274684)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250327-linux-x86_64-python-8a00c9a4d2ce9d373b13-3.14.0a6%2B-8a00c9a.json)

### vs. 3.12.6

- Geometric mean: 1.139x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250327-linux-x86_64-python-8a00c9a4d2ce9d373b13-3.14.0a6%2B-8a00c9a-vs-3.12.6.md)
- [📈time plot](bm-20250327-linux-x86_64-python-8a00c9a4d2ce9d373b13-3.14.0a6%2B-8a00c9a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.092x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250327-linux-x86_64-python-8a00c9a4d2ce9d373b13-3.14.0a6%2B-8a00c9a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250327-linux-x86_64-python-8a00c9a4d2ce9d373b13-3.14.0a6%2B-8a00c9a-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14119274684)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250327-vultr-x86_64-python-8a00c9a4d2ce9d373b13-3.14.0a6%2B-8a00c9a.json)

### vs. 3.12.6

- Geometric mean: 1.109x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250327-vultr-x86_64-python-8a00c9a4d2ce9d373b13-3.14.0a6%2B-8a00c9a-vs-3.12.6.md)
- [📈time plot](bm-20250327-vultr-x86_64-python-8a00c9a4d2ce9d373b13-3.14.0a6%2B-8a00c9a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.069x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250327-vultr-x86_64-python-8a00c9a4d2ce9d373b13-3.14.0a6%2B-8a00c9a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250327-vultr-x86_64-python-8a00c9a4d2ce9d373b13-3.14.0a6%2B-8a00c9a-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14119274684)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6%2B-8a00c9a.json)

### vs. 3.12.6

- Geometric mean: 1.035x faster (HPT: reliability of 52.52%, 1.00x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6%2B-8a00c9a-vs-3.12.6.md)
- [📈time plot](bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6%2B-8a00c9a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.040x slower (HPT: reliability of 99.23%, 1.00x slower at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6%2B-8a00c9a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6%2B-8a00c9a-vs-3.13.0rc2.svg)

