# Results

- fork: python/732d1b02417e91d6a424
- version: 3.14.0a7+
- config: 
- commit hash: [732d1b0](https://github.com/python/cpython/commit/732d1b0)
- commit date: 2025-04-29T17:21:53-07:00
- commit merge base: [b329096cfbebb60e0f5c3ea0a300f650d2004200](https://github.com/python/cpython/commit/b329096cfbebb60e0f5c3ea0a300f650d2004200)
- ref: 732d1b02417e91d6a424

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14744000233)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-6.8.0-1024-aws-x86_64-with-glibc2.35
- [raw results](bm-20250429-linux-x86_64-python-732d1b02417e91d6a424-3.14.0a7%2B-732d1b0.json)

### vs. 3.12.6

- Geometric mean: 1.181x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250429-linux-x86_64-python-732d1b02417e91d6a424-3.14.0a7%2B-732d1b0-vs-3.12.6.md)
- [📈time plot](bm-20250429-linux-x86_64-python-732d1b02417e91d6a424-3.14.0a7%2B-732d1b0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.137x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250429-linux-x86_64-python-732d1b02417e91d6a424-3.14.0a7%2B-732d1b0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250429-linux-x86_64-python-732d1b02417e91d6a424-3.14.0a7%2B-732d1b0-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14744000233)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250429-vultr-x86_64-python-732d1b02417e91d6a424-3.14.0a7%2B-732d1b0.json)

### vs. 3.12.6

- Geometric mean: 1.121x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250429-vultr-x86_64-python-732d1b02417e91d6a424-3.14.0a7%2B-732d1b0-vs-3.12.6.md)
- [📈time plot](bm-20250429-vultr-x86_64-python-732d1b02417e91d6a424-3.14.0a7%2B-732d1b0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.081x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250429-vultr-x86_64-python-732d1b02417e91d6a424-3.14.0a7%2B-732d1b0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250429-vultr-x86_64-python-732d1b02417e91d6a424-3.14.0a7%2B-732d1b0-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14744000233)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250429-macm4pro-arm64-python-732d1b02417e91d6a424-3.14.0a7%2B-732d1b0.json)

### vs. 3.12.6

- Geometric mean: 1.107x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250429-macm4pro-arm64-python-732d1b02417e91d6a424-3.14.0a7%2B-732d1b0-vs-3.12.6.md)
- [📈time plot](bm-20250429-macm4pro-arm64-python-732d1b02417e91d6a424-3.14.0a7%2B-732d1b0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.027x faster (HPT: reliability of 73.23%, 1.00x faster at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250429-macm4pro-arm64-python-732d1b02417e91d6a424-3.14.0a7%2B-732d1b0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250429-macm4pro-arm64-python-732d1b02417e91d6a424-3.14.0a7%2B-732d1b0-vs-3.13.0rc2.svg)

