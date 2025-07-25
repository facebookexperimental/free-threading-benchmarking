# Results

- fork: python/d5e75c07682864e9d265
- version: 3.15.0a0
- config: NOGIL
- commit hash: [d5e75c0](https://github.com/python/cpython/commit/d5e75c0)
- commit date: 2025-07-24T15:50:01-05:00
- commit merge base: [9a6b60af409d02468b935c569a4f49e88c399c4e](https://github.com/python/cpython/commit/9a6b60af409d02468b935c569a4f49e88c399c4e)
- ref: d5e75c07682864e9d265

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16510804001)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250724-vultr-x86_64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0.json)

### vs. 3.12.6

- Geometric mean: 1.029x slower (HPT: reliability of 98.13%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250724-vultr-x86_64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.12.6.md)
- [📈time plot](bm-20250724-vultr-x86_64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.061x slower (HPT: reliability of 98.55%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250724-vultr-x86_64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250724-vultr-x86_64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.091x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250724-vultr-x86_64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-base-mem.svg)
- [📄table](bm-20250724-vultr-x86_64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-base.md)
- [📈time plot](bm-20250724-vultr-x86_64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16510804001)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250724-macm4pro-arm64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0.json)

### vs. 3.12.6

- Geometric mean: 1.087x faster (HPT: reliability of 95.78%, 1.00x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250724-macm4pro-arm64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.12.6.md)
- [📈time plot](bm-20250724-macm4pro-arm64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.008x faster (HPT: reliability of 72.12%, 1.00x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250724-macm4pro-arm64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250724-macm4pro-arm64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.007x slower (HPT: reliability of 93.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250724-macm4pro-arm64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-base-mem.svg)
- [📄table](bm-20250724-macm4pro-arm64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-base.md)
- [📈time plot](bm-20250724-macm4pro-arm64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-base.svg)

