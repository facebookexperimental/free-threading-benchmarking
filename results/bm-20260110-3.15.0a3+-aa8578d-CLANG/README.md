# Results

- fork: python/aa8578dc54df2af9daa3
- version: 3.15.0a3+
- config: CLANG
- commit hash: [aa8578d](https://github.com/python/cpython/commit/aa8578d)
- commit date: 2026-01-10T14:34:30+01:00
- commit merge base: [ce6bae92da671e31013b00901591ce2b595b61ce](https://github.com/python/cpython/commit/ce6bae92da671e31013b00901591ce2b595b61ce)
- ref: aa8578dc54df2af9daa3

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20886568261)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d.json)

### vs. 3.12.6

- Geometric mean: 1.136x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-vs-3.12.6.md)
- [📈time plot](bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.099x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.059x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-vs-base-mem.svg)
- [📄table](bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-vs-base.md)
- [📈time plot](bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20886568261)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d.json)

### vs. 3.12.6

- Geometric mean: 1.187x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-vs-3.12.6.md)
- [📈time plot](bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.101x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.026x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-vs-base-mem.svg)
- [📄table](bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-vs-base.md)
- [📈time plot](bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-vs-base.svg)

