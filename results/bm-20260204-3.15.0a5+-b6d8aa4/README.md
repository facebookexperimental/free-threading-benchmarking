# Results

- fork: python/b6d8aa436b0108fcc90c
- version: 3.15.0a5+
- config: 
- commit hash: [b6d8aa4](https://github.com/python/cpython/commit/b6d8aa4)
- commit date: 2026-02-04T14:21:20-06:00
- commit merge base: [009c8c052f5eb9f869c09029724ef194d8c161ca](https://github.com/python/cpython/commit/009c8c052f5eb9f869c09029724ef194d8c161ca)
- ref: b6d8aa436b0108fcc90c

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21694055374)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260204-vultr-x86_64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4.json)

### vs. 3.12.6

- Geometric mean: 1.083x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260204-vultr-x86_64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.12.6.md)
- [📈time plot](bm-20260204-vultr-x86_64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.047x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260204-vultr-x86_64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.13.0rc2.md)
- [📈time plot](bm-20260204-vultr-x86_64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21694055374)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4.json)

### vs. 3.12.6

- Geometric mean: 1.196x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.12.6.md)
- [📈time plot](bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.110x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.13.0rc2.md)
- [📈time plot](bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.13.0rc2.svg)

