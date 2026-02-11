# Results

- fork: python/d18dbd5e1ce6ca43b559
- version: 3.15.0a5+
- config: NOGIL
- commit hash: [d18dbd5](https://github.com/python/cpython/commit/d18dbd5)
- commit date: 2026-02-10T23:09:07Z
- commit merge base: [87c9789b9a067caf84a0e70093c798525732f8a1](https://github.com/python/cpython/commit/87c9789b9a067caf84a0e70093c798525732f8a1)
- commit date: 2026-02-10T23:09:07+00:00
- ref: d18dbd5e1ce6ca43b559

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21888176584)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5%2B-d18dbd5.json)

### vs. 3.12.6

- Geometric mean: 1.033x slower (HPT: reliability of 76.70%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5%2B-d18dbd5-vs-3.12.6.md)
- [📈time plot](bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5%2B-d18dbd5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.066x slower (HPT: reliability of 95.87%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5%2B-d18dbd5-vs-3.13.0rc2.md)
- [📈time plot](bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5%2B-d18dbd5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.102x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5%2B-d18dbd5-vs-base-mem.svg)
- [📄table](bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5%2B-d18dbd5-vs-base.md)
- [📈time plot](bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5%2B-d18dbd5-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21888176584)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5%2B-d18dbd5.json)

### vs. 3.12.6

- Geometric mean: 1.110x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5%2B-d18dbd5-vs-3.12.6.md)
- [📈time plot](bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5%2B-d18dbd5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.030x faster (HPT: reliability of 76.54%, 1.00x faster at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5%2B-d18dbd5-vs-3.13.0rc2.md)
- [📈time plot](bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5%2B-d18dbd5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.054x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5%2B-d18dbd5-vs-base-mem.svg)
- [📄table](bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5%2B-d18dbd5-vs-base.md)
- [📈time plot](bm-20260210-macm4pro-arm64-python-d18dbd5e1ce6ca43b559-3.15.0a5%2B-d18dbd5-vs-base.svg)

