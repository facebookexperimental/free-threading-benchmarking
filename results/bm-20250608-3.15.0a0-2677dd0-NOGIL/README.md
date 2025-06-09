# Results

- fork: python/2677dd017a033eaaad3b
- version: 3.15.0a0
- config: NOGIL
- commit hash: [2677dd0](https://github.com/python/cpython/commit/2677dd0)
- commit date: 2025-06-08T15:28:37-07:00
- commit merge base: [8d17a412da7e7d8412efc625d48dcb5eecea50b0](https://github.com/python/cpython/commit/8d17a412da7e7d8412efc625d48dcb5eecea50b0)
- ref: 2677dd017a033eaaad3b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15524134542)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250608-vultr-x86_64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0.json)

### vs. 3.12.6

- Geometric mean: 1.012x faster (HPT: reliability of 90.64%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250608-vultr-x86_64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0-vs-3.12.6.md)
- [📈time plot](bm-20250608-vultr-x86_64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.023x slower (HPT: reliability of 96.16%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250608-vultr-x86_64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250608-vultr-x86_64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.094x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250608-vultr-x86_64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0-vs-base-mem.svg)
- [📄table](bm-20250608-vultr-x86_64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0-vs-base.md)
- [📈time plot](bm-20250608-vultr-x86_64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15524134542)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0.json)

### vs. 3.12.6

- Geometric mean: 1.106x faster (HPT: reliability of 99.64%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0-vs-3.12.6.md)
- [📈time plot](bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.025x faster (HPT: reliability of 50.98%, 1.00x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.026x slower (HPT: reliability of 99.49%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0-vs-base-mem.svg)
- [📄table](bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0-vs-base.md)
- [📈time plot](bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0-vs-base.svg)

