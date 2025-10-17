# Results

- fork: python/9a87ce8b57f5d698900d
- version: 3.15.0a1+
- config: NOGIL
- commit hash: [9a87ce8](https://github.com/python/cpython/commit/9a87ce8)
- commit date: 2025-10-16T23:57:51+05:30
- commit merge base: [2ebd0cdb16a8824957ea588e1aab0a35d45e6b7b](https://github.com/python/cpython/commit/2ebd0cdb16a8824957ea588e1aab0a35d45e6b7b)
- ref: 9a87ce8b57f5d698900d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18578590137)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251016-vultr-x86_64-python-9a87ce8b57f5d698900d-3.15.0a1%2B-9a87ce8.json)

### vs. 3.12.6

- Geometric mean: 1.014x slower (HPT: reliability of 79.53%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251016-vultr-x86_64-python-9a87ce8b57f5d698900d-3.15.0a1%2B-9a87ce8-vs-3.12.6.md)
- [📈time plot](bm-20251016-vultr-x86_64-python-9a87ce8b57f5d698900d-3.15.0a1%2B-9a87ce8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.047x slower (HPT: reliability of 92.35%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251016-vultr-x86_64-python-9a87ce8b57f5d698900d-3.15.0a1%2B-9a87ce8-vs-3.13.0rc2.md)
- [📈time plot](bm-20251016-vultr-x86_64-python-9a87ce8b57f5d698900d-3.15.0a1%2B-9a87ce8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.084x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20251016-vultr-x86_64-python-9a87ce8b57f5d698900d-3.15.0a1%2B-9a87ce8-vs-base-mem.svg)
- [📄table](bm-20251016-vultr-x86_64-python-9a87ce8b57f5d698900d-3.15.0a1%2B-9a87ce8-vs-base.md)
- [📈time plot](bm-20251016-vultr-x86_64-python-9a87ce8b57f5d698900d-3.15.0a1%2B-9a87ce8-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18578590137)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251016-macm4pro-arm64-python-9a87ce8b57f5d698900d-3.15.0a1%2B-9a87ce8.json)

### vs. 3.12.6

- Geometric mean: 1.079x faster (HPT: reliability of 96.38%, 1.00x faster at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251016-macm4pro-arm64-python-9a87ce8b57f5d698900d-3.15.0a1%2B-9a87ce8-vs-3.12.6.md)
- [📈time plot](bm-20251016-macm4pro-arm64-python-9a87ce8b57f5d698900d-3.15.0a1%2B-9a87ce8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.001x faster (HPT: reliability of 76.08%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251016-macm4pro-arm64-python-9a87ce8b57f5d698900d-3.15.0a1%2B-9a87ce8-vs-3.13.0rc2.md)
- [📈time plot](bm-20251016-macm4pro-arm64-python-9a87ce8b57f5d698900d-3.15.0a1%2B-9a87ce8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.023x slower (HPT: reliability of 99.42%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- [🧠memory plot](bm-20251016-macm4pro-arm64-python-9a87ce8b57f5d698900d-3.15.0a1%2B-9a87ce8-vs-base-mem.svg)
- [📄table](bm-20251016-macm4pro-arm64-python-9a87ce8b57f5d698900d-3.15.0a1%2B-9a87ce8-vs-base.md)
- [📈time plot](bm-20251016-macm4pro-arm64-python-9a87ce8b57f5d698900d-3.15.0a1%2B-9a87ce8-vs-base.svg)

