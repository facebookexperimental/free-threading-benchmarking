# Results

- fork: python/aa8578dc54df2af9daa3
- version: 3.15.0a3+
- config: 
- commit hash: [aa8578d](https://github.com/python/cpython/commit/aa8578d)
- commit date: 2026-01-10T14:34:30+01:00
- commit merge base: [ce6bae92da671e31013b00901591ce2b595b61ce](https://github.com/python/cpython/commit/ce6bae92da671e31013b00901591ce2b595b61ce)
- ref: aa8578dc54df2af9daa3

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20886568261)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-pystats.json)
- [pystats table](bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-pystats.md)
- [raw results](bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d.json)

### vs. 3.12.6

- Geometric mean: 1.071x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-vs-3.12.6.md)
- [📈time plot](bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.035x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260110-vultr-x86_64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20886568261)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d.json)

### vs. 3.12.6

- Geometric mean: 1.158x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-vs-3.12.6.md)
- [📈time plot](bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.074x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3%2B-aa8578d-vs-3.13.0rc2.svg)

