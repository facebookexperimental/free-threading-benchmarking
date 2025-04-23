# Results

- fork: python/b5bf8c80a921679b2354
- version: 3.14.0a7+
- config: 
- commit hash: [b5bf8c8](https://github.com/python/cpython/commit/b5bf8c8)
- commit date: 2025-04-22T17:37:20-06:00
- commit merge base: [a4ea80d52394bafffb2257abbe815c7ffdb003a3](https://github.com/python/cpython/commit/a4ea80d52394bafffb2257abbe815c7ffdb003a3)
- ref: b5bf8c80a921679b2354

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14607205756)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250422-linux-x86_64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8.json)

### vs. 3.12.6

- Geometric mean: 1.227x faster (HPT: reliability of 100.00%, 1.13x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250422-linux-x86_64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8-vs-3.12.6.md)
- [📈time plot](bm-20250422-linux-x86_64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.179x faster (HPT: reliability of 100.00%, 1.12x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250422-linux-x86_64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8-vs-3.13.0rc2.md)
- [📈time plot](bm-20250422-linux-x86_64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14607205756)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250422-vultr-x86_64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8.json)

### vs. 3.12.6

- Geometric mean: 1.112x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250422-vultr-x86_64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8-vs-3.12.6.md)
- [📈time plot](bm-20250422-vultr-x86_64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.073x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250422-vultr-x86_64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8-vs-3.13.0rc2.md)
- [📈time plot](bm-20250422-vultr-x86_64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14607205756)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250422-macm4pro-arm64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8.json)

### vs. 3.12.6

- Geometric mean: 1.095x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250422-macm4pro-arm64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8-vs-3.12.6.md)
- [📈time plot](bm-20250422-macm4pro-arm64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.016x faster (HPT: reliability of 55.46%, 1.00x slower at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250422-macm4pro-arm64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8-vs-3.13.0rc2.md)
- [📈time plot](bm-20250422-macm4pro-arm64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8-vs-3.13.0rc2.svg)

