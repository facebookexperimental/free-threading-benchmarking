# Results

- fork: python/9752c840229fa6329d12
- version: 3.14.0a7+
- config: 
- commit hash: [9752c84](https://github.com/python/cpython/commit/9752c84)
- commit date: 2025-04-18T15:27:32-07:00
- commit merge base: [ce31ae5209c976d28d1c21fcbb06c0ae5e50a896](https://github.com/python/cpython/commit/ce31ae5209c976d28d1c21fcbb06c0ae5e50a896)
- ref: 9752c840229fa6329d12

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14543774435)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250418-linux-x86_64-python-9752c840229fa6329d12-3.14.0a7%2B-9752c84.json)

### vs. 3.12.6

- Geometric mean: 1.231x faster (HPT: reliability of 100.00%, 1.13x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250418-linux-x86_64-python-9752c840229fa6329d12-3.14.0a7%2B-9752c84-vs-3.12.6.md)
- [📈time plot](bm-20250418-linux-x86_64-python-9752c840229fa6329d12-3.14.0a7%2B-9752c84-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.183x faster (HPT: reliability of 100.00%, 1.11x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250418-linux-x86_64-python-9752c840229fa6329d12-3.14.0a7%2B-9752c84-vs-3.13.0rc2.md)
- [📈time plot](bm-20250418-linux-x86_64-python-9752c840229fa6329d12-3.14.0a7%2B-9752c84-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14543774435)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250418-vultr-x86_64-python-9752c840229fa6329d12-3.14.0a7%2B-9752c84.json)

### vs. 3.12.6

- Geometric mean: 1.107x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250418-vultr-x86_64-python-9752c840229fa6329d12-3.14.0a7%2B-9752c84-vs-3.12.6.md)
- [📈time plot](bm-20250418-vultr-x86_64-python-9752c840229fa6329d12-3.14.0a7%2B-9752c84-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.067x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250418-vultr-x86_64-python-9752c840229fa6329d12-3.14.0a7%2B-9752c84-vs-3.13.0rc2.md)
- [📈time plot](bm-20250418-vultr-x86_64-python-9752c840229fa6329d12-3.14.0a7%2B-9752c84-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14543774435)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250418-macm4pro-arm64-python-9752c840229fa6329d12-3.14.0a7%2B-9752c84.json)

### vs. 3.12.6

- Geometric mean: 1.103x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250418-macm4pro-arm64-python-9752c840229fa6329d12-3.14.0a7%2B-9752c84-vs-3.12.6.md)
- [📈time plot](bm-20250418-macm4pro-arm64-python-9752c840229fa6329d12-3.14.0a7%2B-9752c84-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.023x faster (HPT: reliability of 65.85%, 1.00x faster at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250418-macm4pro-arm64-python-9752c840229fa6329d12-3.14.0a7%2B-9752c84-vs-3.13.0rc2.md)
- [📈time plot](bm-20250418-macm4pro-arm64-python-9752c840229fa6329d12-3.14.0a7%2B-9752c84-vs-3.13.0rc2.svg)

