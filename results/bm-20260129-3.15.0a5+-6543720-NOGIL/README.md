# Results

- fork: python/6543720b63a62363de54
- version: 3.15.0a5+
- config: NOGIL
- commit hash: [6543720](https://github.com/python/cpython/commit/6543720)
- commit date: 2026-01-29T07:48:26+08:00
- commit merge base: [9b154aba7d08c0b5c72d1e415097852388e6d87b](https://github.com/python/cpython/commit/9b154aba7d08c0b5c72d1e415097852388e6d87b)
- ref: 6543720b63a62363de54

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21460941798)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260129-vultr-x86_64-python-6543720b63a62363de54-3.15.0a5%2B-6543720.json)

### vs. 3.12.6

- Geometric mean: 1.027x slower (HPT: reliability of 77.57%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260129-vultr-x86_64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.12.6.md)
- [📈time plot](bm-20260129-vultr-x86_64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.060x slower (HPT: reliability of 86.91%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260129-vultr-x86_64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.13.0rc2.md)
- [📈time plot](bm-20260129-vultr-x86_64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.102x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20260129-vultr-x86_64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-base-mem.svg)
- [📄table](bm-20260129-vultr-x86_64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-base.md)
- [📈time plot](bm-20260129-vultr-x86_64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21460941798)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260129-macm4pro-arm64-python-6543720b63a62363de54-3.15.0a5%2B-6543720.json)

### vs. 3.12.6

- Geometric mean: 1.114x faster (HPT: reliability of 99.98%, 1.02x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260129-macm4pro-arm64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.12.6.md)
- [📈time plot](bm-20260129-macm4pro-arm64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.033x faster (HPT: reliability of 79.50%, 1.00x faster at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260129-macm4pro-arm64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.13.0rc2.md)
- [📈time plot](bm-20260129-macm4pro-arm64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.069x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20260129-macm4pro-arm64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-base-mem.svg)
- [📄table](bm-20260129-macm4pro-arm64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-base.md)
- [📈time plot](bm-20260129-macm4pro-arm64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-base.svg)

