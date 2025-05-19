# Results

- fork: python/9983c7d4416cac8deb2f
- version: 3.15.0a0
- config: NOGIL
- commit hash: [9983c7d](https://github.com/python/cpython/commit/9983c7d)
- commit date: 2025-05-18T22:21:06+03:00
- commit merge base: [5cbc8c632e860941602e8f7da9aab52fae40aca6](https://github.com/python/cpython/commit/5cbc8c632e860941602e8f7da9aab52fae40aca6)
- ref: 9983c7d4416cac8deb2f

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15101644693)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-6.8.0-1024-aws-x86_64-with-glibc2.35
- [raw results](bm-20250518-linux-x86_64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d.json)

### vs. 3.12.6

- Geometric mean: 1.134x faster (HPT: reliability of 98.67%, 1.00x faster at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250518-linux-x86_64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d-vs-3.12.6.md)
- [📈time plot](bm-20250518-linux-x86_64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.092x faster (HPT: reliability of 96.58%, 1.00x faster at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250518-linux-x86_64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250518-linux-x86_64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.083x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250518-linux-x86_64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d-vs-base-mem.svg)
- [📄table](bm-20250518-linux-x86_64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d-vs-base.md)
- [📈time plot](bm-20250518-linux-x86_64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15101644693)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250518-vultr-x86_64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d.json)

### vs. 3.12.6

- Geometric mean: 1.016x faster (HPT: reliability of 90.32%, 1.00x slower at 99th %ile)
- Memory usage: 1.44x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250518-vultr-x86_64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d-vs-3.12.6.md)
- [📈time plot](bm-20250518-vultr-x86_64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.020x slower (HPT: reliability of 95.05%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250518-vultr-x86_64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250518-vultr-x86_64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.093x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250518-vultr-x86_64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d-vs-base-mem.svg)
- [📄table](bm-20250518-vultr-x86_64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d-vs-base.md)
- [📈time plot](bm-20250518-vultr-x86_64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15101644693)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d.json)

### vs. 3.12.6

- Geometric mean: 1.083x faster (HPT: reliability of 96.75%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d-vs-3.12.6.md)
- [📈time plot](bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.004x faster (HPT: reliability of 77.29%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.025x slower (HPT: reliability of 99.37%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d-vs-base-mem.svg)
- [📄table](bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d-vs-base.md)
- [📈time plot](bm-20250518-macm4pro-arm64-python-9983c7d4416cac8deb2f-3.15.0a0-9983c7d-vs-base.svg)

