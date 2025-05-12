# Results

- fork: python/0eb448cae5e9008f8152
- version: 3.15.0a0
- config: NOGIL
- commit hash: [0eb448c](https://github.com/python/cpython/commit/0eb448c)
- commit date: 2025-05-11T08:43:24-07:00
- commit merge base: [3396df56d0849e5154cb7d7d1c525df834bbe15e](https://github.com/python/cpython/commit/3396df56d0849e5154cb7d7d1c525df834bbe15e)
- ref: 0eb448cae5e9008f8152

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14961238629)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-6.8.0-1024-aws-x86_64-with-glibc2.35
- [raw results](bm-20250511-linux-x86_64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c.json)

### vs. 3.12.6

- Geometric mean: 1.119x faster (HPT: reliability of 95.61%, 1.00x faster at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250511-linux-x86_64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c-vs-3.12.6.md)
- [📈time plot](bm-20250511-linux-x86_64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.078x faster (HPT: reliability of 89.11%, 1.00x faster at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250511-linux-x86_64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c-vs-3.13.0rc2.md)
- [📈time plot](bm-20250511-linux-x86_64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.086x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20250511-linux-x86_64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c-vs-base-mem.svg)
- [📄table](bm-20250511-linux-x86_64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c-vs-base.md)
- [📈time plot](bm-20250511-linux-x86_64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14961238629)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250511-vultr-x86_64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c.json)

### vs. 3.12.6

- Geometric mean: 1.011x faster (HPT: reliability of 87.42%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250511-vultr-x86_64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c-vs-3.12.6.md)
- [📈time plot](bm-20250511-vultr-x86_64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.023x slower (HPT: reliability of 95.34%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250511-vultr-x86_64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c-vs-3.13.0rc2.md)
- [📈time plot](bm-20250511-vultr-x86_64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.091x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250511-vultr-x86_64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c-vs-base-mem.svg)
- [📄table](bm-20250511-vultr-x86_64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c-vs-base.md)
- [📈time plot](bm-20250511-vultr-x86_64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14961238629)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250511-macm4pro-arm64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c.json)

### vs. 3.12.6

- Geometric mean: 1.072x faster (HPT: reliability of 85.32%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250511-macm4pro-arm64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c-vs-3.12.6.md)
- [📈time plot](bm-20250511-macm4pro-arm64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.006x slower (HPT: reliability of 88.80%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250511-macm4pro-arm64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c-vs-3.13.0rc2.md)
- [📈time plot](bm-20250511-macm4pro-arm64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.010x slower (HPT: reliability of 95.63%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250511-macm4pro-arm64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c-vs-base-mem.svg)
- [📄table](bm-20250511-macm4pro-arm64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c-vs-base.md)
- [📈time plot](bm-20250511-macm4pro-arm64-python-0eb448cae5e9008f8152-3.15.0a0-0eb448c-vs-base.svg)

