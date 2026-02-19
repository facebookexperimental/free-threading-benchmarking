# Results

- fork: python/0bbdb4e897ae909af39c
- version: 3.15.0a6+
- config: NOGIL
- commit hash: [0bbdb4e](https://github.com/python/cpython/commit/0bbdb4e)
- commit date: 2026-02-18T20:23:49Z
- commit merge base: [16ccdbc50a3034f9c0e5ea6845356281b2ad04bd](https://github.com/python/cpython/commit/16ccdbc50a3034f9c0e5ea6845356281b2ad04bd)
- commit date: 2026-02-18T20:23:49+00:00
- ref: 0bbdb4e897ae909af39c

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22163648819)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6%2B-0bbdb4e.json)

### vs. 3.12.6

- Geometric mean: 1.031x slower (HPT: reliability of 75.51%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6%2B-0bbdb4e-vs-3.12.6.md)
- [📈time plot](bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6%2B-0bbdb4e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.063x slower (HPT: reliability of 92.22%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6%2B-0bbdb4e-vs-3.13.0rc2.md)
- [📈time plot](bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6%2B-0bbdb4e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.108x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6%2B-0bbdb4e-vs-base-mem.svg)
- [📄table](bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6%2B-0bbdb4e-vs-base.md)
- [📈time plot](bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6%2B-0bbdb4e-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22163648819)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6%2B-0bbdb4e.json)

### vs. 3.12.6

- Geometric mean: 1.091x faster (HPT: reliability of 99.84%, 1.00x faster at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6%2B-0bbdb4e-vs-3.12.6.md)
- [📈time plot](bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6%2B-0bbdb4e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.012x faster (HPT: reliability of 54.87%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6%2B-0bbdb4e-vs-3.13.0rc2.md)
- [📈time plot](bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6%2B-0bbdb4e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.033x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6%2B-0bbdb4e-vs-base-mem.svg)
- [📄table](bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6%2B-0bbdb4e-vs-base.md)
- [📈time plot](bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6%2B-0bbdb4e-vs-base.svg)

