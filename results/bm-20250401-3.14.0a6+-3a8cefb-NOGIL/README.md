# Results

- fork: python/3a8cefba0b60bd25c6b1
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [3a8cefb](https://github.com/python/cpython/commit/3a8cefb)
- commit date: 2025-04-01T16:55:05-07:00
- commit merge base: [1a9d4a1fb3d4beda7c7e8483af7c6bc7ac477e9f](https://github.com/python/cpython/commit/1a9d4a1fb3d4beda7c7e8483af7c6bc7ac477e9f)
- ref: 3a8cefba0b60bd25c6b1

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14208761861)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb.json)

### vs. 3.12.6

- Geometric mean: 1.038x faster (HPT: reliability of 51.41%, 1.00x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-3.12.6.md)
- [📈time plot](bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.003x faster (HPT: reliability of 75.15%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-3.13.0rc2.md)
- [📈time plot](bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.082x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-base-mem.svg)
- [📄table](bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-base.md)
- [📈time plot](bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14208761861)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb.json)

### vs. 3.12.6

- Geometric mean: 1.082x slower (HPT: reliability of 99.99%, 1.07x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-3.12.6.md)
- [📈time plot](bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.112x slower (HPT: reliability of 99.99%, 1.08x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-3.13.0rc2.md)
- [📈time plot](bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.146x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-base-mem.svg)
- [📄table](bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-base.md)
- [📈time plot](bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14208761861)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb.json)

### vs. 3.12.6

- Geometric mean: 1.028x faster (HPT: reliability of 84.46%, 1.00x slower at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-3.12.6.md)
- [📈time plot](bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.046x slower (HPT: reliability of 99.19%, 1.00x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-3.13.0rc2.md)
- [📈time plot](bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.071x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-base-mem.svg)
- [📄table](bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-base.md)
- [📈time plot](bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-base.svg)

