# Results

- fork: python/6eaa4aeef25f77a31768
- version: 3.14.0a6+
- config: 
- commit hash: [6eaa4ae](https://github.com/python/cpython/commit/6eaa4ae)
- commit date: 2025-04-07T00:36:21+01:00
- commit merge base: [e2476398ee9911b6b0b80e3ca182647805fde81f](https://github.com/python/cpython/commit/e2476398ee9911b6b0b80e3ca182647805fde81f)
- ref: 6eaa4aeef25f77a31768

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14298182104)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250407-linux-x86_64-python-6eaa4aeef25f77a31768-3.14.0a6%2B-6eaa4ae.json)

### vs. 3.12.6

- Geometric mean: 1.142x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250407-linux-x86_64-python-6eaa4aeef25f77a31768-3.14.0a6%2B-6eaa4ae-vs-3.12.6.md)
- [📈time plot](bm-20250407-linux-x86_64-python-6eaa4aeef25f77a31768-3.14.0a6%2B-6eaa4ae-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.097x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250407-linux-x86_64-python-6eaa4aeef25f77a31768-3.14.0a6%2B-6eaa4ae-vs-3.13.0rc2.md)
- [📈time plot](bm-20250407-linux-x86_64-python-6eaa4aeef25f77a31768-3.14.0a6%2B-6eaa4ae-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14298182104)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250407-vultr-x86_64-python-6eaa4aeef25f77a31768-3.14.0a6%2B-6eaa4ae.json)

### vs. 3.12.6

- Geometric mean: 1.078x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250407-vultr-x86_64-python-6eaa4aeef25f77a31768-3.14.0a6%2B-6eaa4ae-vs-3.12.6.md)
- [📈time plot](bm-20250407-vultr-x86_64-python-6eaa4aeef25f77a31768-3.14.0a6%2B-6eaa4ae-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.040x faster (HPT: reliability of 95.96%, 1.00x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250407-vultr-x86_64-python-6eaa4aeef25f77a31768-3.14.0a6%2B-6eaa4ae-vs-3.13.0rc2.md)
- [📈time plot](bm-20250407-vultr-x86_64-python-6eaa4aeef25f77a31768-3.14.0a6%2B-6eaa4ae-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14298182104)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6%2B-6eaa4ae.json)

### vs. 3.12.6

- Geometric mean: 1.109x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6%2B-6eaa4ae-vs-3.12.6.md)
- [📈time plot](bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6%2B-6eaa4ae-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.029x faster (HPT: reliability of 78.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6%2B-6eaa4ae-vs-3.13.0rc2.md)
- [📈time plot](bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6%2B-6eaa4ae-vs-3.13.0rc2.svg)

