# Results

- fork: python/9ad0c7b0f14c5fcda6bf
- version: 3.15.0a0
- config: NOGIL
- commit hash: [9ad0c7b](https://github.com/python/cpython/commit/9ad0c7b)
- commit date: 2025-05-13T17:38:57Z
- commit merge base: [35f47d05893e012e9f2b145b934c1d8c61d2bb7d](https://github.com/python/cpython/commit/35f47d05893e012e9f2b145b934c1d8c61d2bb7d)
- commit date: 2025-05-13T17:38:57+00:00
- ref: 9ad0c7b0f14c5fcda6bf

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15009450205)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-6.8.0-1024-aws-x86_64-with-glibc2.35
- [raw results](bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json)

### vs. 3.12.6

- Geometric mean: 1.114x faster (HPT: reliability of 93.64%, 1.00x faster at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b-vs-3.12.6.md)
- [📈time plot](bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.073x faster (HPT: reliability of 82.89%, 1.00x faster at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.086x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b-vs-base-mem.svg)
- [📄table](bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b-vs-base.md)
- [📈time plot](bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15009450205)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json)

### vs. 3.12.6

- Geometric mean: 1.015x faster (HPT: reliability of 90.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b-vs-3.12.6.md)
- [📈time plot](bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.020x slower (HPT: reliability of 95.70%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.090x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.23x
- [🧠memory plot](bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b-vs-base-mem.svg)
- [📄table](bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b-vs-base.md)
- [📈time plot](bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15009450205)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json)

### vs. 3.12.6

- Geometric mean: 1.075x faster (HPT: reliability of 86.74%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b-vs-3.12.6.md)
- [📈time plot](bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.003x slower (HPT: reliability of 89.64%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.014x slower (HPT: reliability of 97.63%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b-vs-base-mem.svg)
- [📄table](bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b-vs-base.md)
- [📈time plot](bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b-vs-base.svg)

