# Results

- fork: python/9d0c7432ea40ab3f73af
- version: 3.15.0a5+
- config: NOGIL
- commit hash: [9d0c743](https://github.com/python/cpython/commit/9d0c743)
- commit date: 2026-02-03T23:38:22Z
- commit merge base: [7e2c9bdc989a2e10e093a18287a107aac7750091](https://github.com/python/cpython/commit/7e2c9bdc989a2e10e093a18287a107aac7750091)
- commit date: 2026-02-03T23:38:22+00:00
- ref: 9d0c7432ea40ab3f73af

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21653473663)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260203-vultr-x86_64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743.json)

### vs. 3.12.6

- Geometric mean: 1.026x slower (HPT: reliability of 78.70%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260203-vultr-x86_64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.12.6.md)
- [📈time plot](bm-20260203-vultr-x86_64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.059x slower (HPT: reliability of 89.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260203-vultr-x86_64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.13.0rc2.md)
- [📈time plot](bm-20260203-vultr-x86_64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.105x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20260203-vultr-x86_64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-base-mem.svg)
- [📄table](bm-20260203-vultr-x86_64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-base.md)
- [📈time plot](bm-20260203-vultr-x86_64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21653473663)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743.json)

### vs. 3.12.6

- Geometric mean: 1.132x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.12.6.md)
- [📈time plot](bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.050x faster (HPT: reliability of 87.96%, 1.00x faster at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.13.0rc2.md)
- [📈time plot](bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.048x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-base-mem.svg)
- [📄table](bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-base.md)
- [📈time plot](bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-base.svg)

