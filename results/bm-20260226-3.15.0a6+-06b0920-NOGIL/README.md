# Results

- fork: python/06b0920f1292690a22ab
- version: 3.15.0a6+
- config: NOGIL
- commit hash: [06b0920](https://github.com/python/cpython/commit/06b0920)
- commit date: 2026-02-26T23:40:25Z
- commit merge base: [3fc945df22a169e039c3f21b44c0d08390a00c0c](https://github.com/python/cpython/commit/3fc945df22a169e039c3f21b44c0d08390a00c0c)
- commit date: 2026-02-26T23:40:25+00:00
- ref: 06b0920f1292690a22ab

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22467526513)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920.json)

### vs. 3.12.6

- Geometric mean: 1.035x slower (HPT: reliability of 78.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.44x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.12.6.md)
- [📈time plot](bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.068x slower (HPT: reliability of 97.43%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.13.0rc2.md)
- [📈time plot](bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.106x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-base-mem.svg)
- [📄table](bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-base.md)
- [📈time plot](bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22467526513)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920.json)

### vs. 3.12.6

- Geometric mean: 1.087x faster (HPT: reliability of 98.31%, 1.00x faster at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.12.6.md)
- [📈time plot](bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.009x faster (HPT: reliability of 70.09%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.13.0rc2.md)
- [📈time plot](bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.059x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-base-mem.svg)
- [📄table](bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-base.md)
- [📈time plot](bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-base.svg)

