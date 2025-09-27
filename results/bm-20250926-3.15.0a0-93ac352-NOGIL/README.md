# Results

- fork: python/93ac3525b92f5f891821
- version: 3.15.0a0
- config: NOGIL
- commit hash: [93ac352](https://github.com/python/cpython/commit/93ac352)
- commit date: 2025-09-26T11:52:10-07:00
- commit merge base: [68a1778b7721f3fb853cd3aa674f7039c2a4df36](https://github.com/python/cpython/commit/68a1778b7721f3fb853cd3aa674f7039c2a4df36)
- ref: 93ac3525b92f5f891821

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18052351601)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250926-vultr-x86_64-python-93ac3525b92f5f891821-3.15.0a0-93ac352.json)

### vs. 3.12.6

- Geometric mean: 1.020x slower (HPT: reliability of 90.64%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250926-vultr-x86_64-python-93ac3525b92f5f891821-3.15.0a0-93ac352-vs-3.12.6.md)
- [📈time plot](bm-20250926-vultr-x86_64-python-93ac3525b92f5f891821-3.15.0a0-93ac352-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.053x slower (HPT: reliability of 96.16%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250926-vultr-x86_64-python-93ac3525b92f5f891821-3.15.0a0-93ac352-vs-3.13.0rc2.md)
- [📈time plot](bm-20250926-vultr-x86_64-python-93ac3525b92f5f891821-3.15.0a0-93ac352-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.094x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20250926-vultr-x86_64-python-93ac3525b92f5f891821-3.15.0a0-93ac352-vs-base-mem.svg)
- [📄table](bm-20250926-vultr-x86_64-python-93ac3525b92f5f891821-3.15.0a0-93ac352-vs-base.md)
- [📈time plot](bm-20250926-vultr-x86_64-python-93ac3525b92f5f891821-3.15.0a0-93ac352-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18052351601)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352.json)

### vs. 3.12.6

- Geometric mean: 1.096x faster (HPT: reliability of 99.32%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352-vs-3.12.6.md)
- [📈time plot](bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.017x faster (HPT: reliability of 54.58%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352-vs-3.13.0rc2.md)
- [📈time plot](bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x faster (HPT: reliability of 85.57%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352-vs-base-mem.svg)
- [📄table](bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352-vs-base.md)
- [📈time plot](bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352-vs-base.svg)

