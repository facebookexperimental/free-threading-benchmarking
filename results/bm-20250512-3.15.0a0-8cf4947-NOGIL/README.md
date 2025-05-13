# Results

- fork: python/8cf4947b0f2d37f7ffec
- version: 3.15.0a0
- config: NOGIL
- commit hash: [8cf4947](https://github.com/python/cpython/commit/8cf4947)
- commit date: 2025-05-12T22:10:56Z
- commit merge base: [121ed71f4e395948d313249b2ad33e1e21581f8a](https://github.com/python/cpython/commit/121ed71f4e395948d313249b2ad33e1e21581f8a)
- commit date: 2025-05-12T22:10:56+00:00
- ref: 8cf4947b0f2d37f7ffec

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14985396477)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-6.8.0-1024-aws-x86_64-with-glibc2.35
- [raw results](bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json)

### vs. 3.12.6

- Geometric mean: 1.120x faster (HPT: reliability of 97.48%, 1.00x faster at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947-vs-3.12.6.md)
- [📈time plot](bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.079x faster (HPT: reliability of 91.34%, 1.00x faster at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947-vs-3.13.0rc2.md)
- [📈time plot](bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.084x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947-vs-base-mem.svg)
- [📄table](bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947-vs-base.md)
- [📈time plot](bm-20250512-linux-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14985396477)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json)

### vs. 3.12.6

- Geometric mean: 1.010x faster (HPT: reliability of 86.29%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947-vs-3.12.6.md)
- [📈time plot](bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.024x slower (HPT: reliability of 96.36%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947-vs-3.13.0rc2.md)
- [📈time plot](bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.094x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.23x
- [🧠memory plot](bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947-vs-base-mem.svg)
- [📄table](bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947-vs-base.md)
- [📈time plot](bm-20250512-vultr-x86_64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14985396477)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947.json)

### vs. 3.12.6

- Geometric mean: 1.073x faster (HPT: reliability of 86.58%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947-vs-3.12.6.md)
- [📈time plot](bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.005x slower (HPT: reliability of 87.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947-vs-3.13.0rc2.md)
- [📈time plot](bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.015x slower (HPT: reliability of 98.23%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947-vs-base-mem.svg)
- [📄table](bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947-vs-base.md)
- [📈time plot](bm-20250512-macm4pro-arm64-python-8cf4947b0f2d37f7ffec-3.15.0a0-8cf4947-vs-base.svg)

