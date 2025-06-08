# Results

- fork: python/8fdbbf8b18f1405abe67
- version: 3.15.0a0
- config: NOGIL
- commit hash: [8fdbbf8](https://github.com/python/cpython/commit/8fdbbf8)
- commit date: 2025-06-07T14:08:44-07:00
- commit merge base: [ac9c3431cc5916a795c42b3e2b965233ceffe6f0](https://github.com/python/cpython/commit/ac9c3431cc5916a795c42b3e2b965233ceffe6f0)
- ref: 8fdbbf8b18f1405abe67

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15512971097)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json)

### vs. 3.12.6

- Geometric mean: 1.011x faster (HPT: reliability of 91.49%, 1.00x slower at 99th %ile)
- Memory usage: 1.44x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8-vs-3.12.6.md)
- [📈time plot](bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.024x slower (HPT: reliability of 96.40%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8-vs-3.13.0rc2.md)
- [📈time plot](bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.088x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8-vs-base-mem.svg)
- [📄table](bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8-vs-base.md)
- [📈time plot](bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15512971097)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json)

### vs. 3.12.6

- Geometric mean: 1.101x faster (HPT: reliability of 99.02%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8-vs-3.12.6.md)
- [📈time plot](bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.020x faster (HPT: reliability of 54.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8-vs-3.13.0rc2.md)
- [📈time plot](bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.020x slower (HPT: reliability of 98.95%, 1.00x slower at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8-vs-base-mem.svg)
- [📄table](bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8-vs-base.md)
- [📈time plot](bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8-vs-base.svg)

