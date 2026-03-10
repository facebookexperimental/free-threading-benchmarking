# Results

- fork: python/099943b122cda2548ad7
- version: 3.15.0a6+
- config: NOGIL
- commit hash: [099943b](https://github.com/python/cpython/commit/099943b)
- commit date: 2026-03-09T22:51:00Z
- commit merge base: [0b65c88c2af6e09530a9aa21800771aa687371db](https://github.com/python/cpython/commit/0b65c88c2af6e09530a9aa21800771aa687371db)
- commit date: 2026-03-09T22:51:00+00:00
- ref: 099943b122cda2548ad7

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22881420119)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260309-vultr-x86_64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b.json)

### vs. 3.12.6

- Geometric mean: 1.029x slower (HPT: reliability of 77.86%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260309-vultr-x86_64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.12.6.md)
- [📈time plot](bm-20260309-vultr-x86_64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.061x slower (HPT: reliability of 95.34%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260309-vultr-x86_64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.13.0rc2.md)
- [📈time plot](bm-20260309-vultr-x86_64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.101x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20260309-vultr-x86_64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-base-mem.svg)
- [📄table](bm-20260309-vultr-x86_64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-base.md)
- [📈time plot](bm-20260309-vultr-x86_64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22881420119)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260309-macm4pro-arm64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b.json)

### vs. 3.12.6

- Geometric mean: 1.091x faster (HPT: reliability of 99.53%, 1.00x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260309-macm4pro-arm64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.12.6.md)
- [📈time plot](bm-20260309-macm4pro-arm64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.012x faster (HPT: reliability of 52.52%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260309-macm4pro-arm64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.13.0rc2.md)
- [📈time plot](bm-20260309-macm4pro-arm64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.039x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.13x
- [🧠memory plot](bm-20260309-macm4pro-arm64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-base-mem.svg)
- [📄table](bm-20260309-macm4pro-arm64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-base.md)
- [📈time plot](bm-20260309-macm4pro-arm64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-base.svg)

