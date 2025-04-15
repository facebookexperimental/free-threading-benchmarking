# Results

- fork: python/0879ebc953fa7372a4d9
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [0879ebc](https://github.com/python/cpython/commit/0879ebc)
- commit date: 2025-04-15T01:05:06+01:00
- commit merge base: [102f825c5112cbe6985edc0971822b07bd778135](https://github.com/python/cpython/commit/102f825c5112cbe6985edc0971822b07bd778135)
- ref: 0879ebc953fa7372a4d9

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14458503058)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250415-linux-x86_64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc.json)

### vs. 3.12.6

- Geometric mean: 1.030x slower (HPT: reliability of 99.58%, 1.01x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250415-linux-x86_64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc-vs-3.12.6.md)
- [📈time plot](bm-20250415-linux-x86_64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.061x slower (HPT: reliability of 99.86%, 1.01x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250415-linux-x86_64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc-vs-3.13.0rc2.md)
- [📈time plot](bm-20250415-linux-x86_64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.117x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250415-linux-x86_64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc-vs-base-mem.svg)
- [📄table](bm-20250415-linux-x86_64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc-vs-base.md)
- [📈time plot](bm-20250415-linux-x86_64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14458503058)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250415-vultr-x86_64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc.json)

### vs. 3.12.6

- Geometric mean: 1.027x faster (HPT: reliability of 71.48%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250415-vultr-x86_64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc-vs-3.12.6.md)
- [📈time plot](bm-20250415-vultr-x86_64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.006x slower (HPT: reliability of 87.76%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250415-vultr-x86_64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc-vs-3.13.0rc2.md)
- [📈time plot](bm-20250415-vultr-x86_64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.079x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250415-vultr-x86_64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc-vs-base-mem.svg)
- [📄table](bm-20250415-vultr-x86_64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc-vs-base.md)
- [📈time plot](bm-20250415-vultr-x86_64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14458503058)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250415-macm4pro-arm64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc.json)

### vs. 3.12.6

- Geometric mean: 1.112x faster (HPT: reliability of 99.83%, 1.01x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250415-macm4pro-arm64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc-vs-3.12.6.md)
- [📈time plot](bm-20250415-macm4pro-arm64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.031x faster (HPT: reliability of 56.49%, 1.00x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250415-macm4pro-arm64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc-vs-3.13.0rc2.md)
- [📈time plot](bm-20250415-macm4pro-arm64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.007x slower (HPT: reliability of 98.90%, 1.00x slower at 99th %ile)
- Memory usage: 1.10x
- [🧠memory plot](bm-20250415-macm4pro-arm64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc-vs-base-mem.svg)
- [📄table](bm-20250415-macm4pro-arm64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc-vs-base.md)
- [📈time plot](bm-20250415-macm4pro-arm64-python-0879ebc953fa7372a4d9-3.14.0a7%2B-0879ebc-vs-base.svg)

