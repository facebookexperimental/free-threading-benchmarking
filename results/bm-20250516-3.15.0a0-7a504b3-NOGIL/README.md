# Results

- fork: python/7a504b3d5da988745368
- version: 3.15.0a0
- config: NOGIL
- commit hash: [7a504b3](https://github.com/python/cpython/commit/7a504b3)
- commit date: 2025-05-16T00:00:06+01:00
- commit merge base: [6a2296329117463fd09abc73656f1d7b48076100](https://github.com/python/cpython/commit/6a2296329117463fd09abc73656f1d7b48076100)
- ref: 7a504b3d5da988745368

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15057874555)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250516-vultr-x86_64-python-7a504b3d5da988745368-3.15.0a0-7a504b3.json)

### vs. 3.12.6

- Geometric mean: 1.005x faster (HPT: reliability of 91.64%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250516-vultr-x86_64-python-7a504b3d5da988745368-3.15.0a0-7a504b3-vs-3.12.6.md)
- [📈time plot](bm-20250516-vultr-x86_64-python-7a504b3d5da988745368-3.15.0a0-7a504b3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.029x slower (HPT: reliability of 98.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250516-vultr-x86_64-python-7a504b3d5da988745368-3.15.0a0-7a504b3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250516-vultr-x86_64-python-7a504b3d5da988745368-3.15.0a0-7a504b3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.100x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250516-vultr-x86_64-python-7a504b3d5da988745368-3.15.0a0-7a504b3-vs-base-mem.svg)
- [📄table](bm-20250516-vultr-x86_64-python-7a504b3d5da988745368-3.15.0a0-7a504b3-vs-base.md)
- [📈time plot](bm-20250516-vultr-x86_64-python-7a504b3d5da988745368-3.15.0a0-7a504b3-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15057874555)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250516-macm4pro-arm64-python-7a504b3d5da988745368-3.15.0a0-7a504b3.json)

### vs. 3.12.6

- Geometric mean: 1.081x faster (HPT: reliability of 95.20%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250516-macm4pro-arm64-python-7a504b3d5da988745368-3.15.0a0-7a504b3-vs-3.12.6.md)
- [📈time plot](bm-20250516-macm4pro-arm64-python-7a504b3d5da988745368-3.15.0a0-7a504b3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.002x faster (HPT: reliability of 75.31%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250516-macm4pro-arm64-python-7a504b3d5da988745368-3.15.0a0-7a504b3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250516-macm4pro-arm64-python-7a504b3d5da988745368-3.15.0a0-7a504b3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.025x slower (HPT: reliability of 99.54%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250516-macm4pro-arm64-python-7a504b3d5da988745368-3.15.0a0-7a504b3-vs-base-mem.svg)
- [📄table](bm-20250516-macm4pro-arm64-python-7a504b3d5da988745368-3.15.0a0-7a504b3-vs-base.md)
- [📈time plot](bm-20250516-macm4pro-arm64-python-7a504b3d5da988745368-3.15.0a0-7a504b3-vs-base.svg)

