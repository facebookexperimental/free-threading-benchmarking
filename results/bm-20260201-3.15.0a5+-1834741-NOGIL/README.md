# Results

- fork: python/18347417b06d09fa7eea
- version: 3.15.0a5+
- config: NOGIL
- commit hash: [1834741](https://github.com/python/cpython/commit/1834741)
- commit date: 2026-02-01T15:25:59+02:00
- commit merge base: [b6256014be7ff8adf100c47c4be8bc002e0607d6](https://github.com/python/cpython/commit/b6256014be7ff8adf100c47c4be8bc002e0607d6)
- ref: 18347417b06d09fa7eea

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21573374608)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260201-vultr-x86_64-python-18347417b06d09fa7eea-3.15.0a5%2B-1834741.json)

### vs. 3.12.6

- Geometric mean: 1.031x slower (HPT: reliability of 80.20%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260201-vultr-x86_64-python-18347417b06d09fa7eea-3.15.0a5%2B-1834741-vs-3.12.6.md)
- [📈time plot](bm-20260201-vultr-x86_64-python-18347417b06d09fa7eea-3.15.0a5%2B-1834741-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.064x slower (HPT: reliability of 92.28%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260201-vultr-x86_64-python-18347417b06d09fa7eea-3.15.0a5%2B-1834741-vs-3.13.0rc2.md)
- [📈time plot](bm-20260201-vultr-x86_64-python-18347417b06d09fa7eea-3.15.0a5%2B-1834741-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.100x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20260201-vultr-x86_64-python-18347417b06d09fa7eea-3.15.0a5%2B-1834741-vs-base-mem.svg)
- [📄table](bm-20260201-vultr-x86_64-python-18347417b06d09fa7eea-3.15.0a5%2B-1834741-vs-base.md)
- [📈time plot](bm-20260201-vultr-x86_64-python-18347417b06d09fa7eea-3.15.0a5%2B-1834741-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21573374608)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260201-macm4pro-arm64-python-18347417b06d09fa7eea-3.15.0a5%2B-1834741.json)

### vs. 3.12.6

- Geometric mean: 1.124x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260201-macm4pro-arm64-python-18347417b06d09fa7eea-3.15.0a5%2B-1834741-vs-3.12.6.md)
- [📈time plot](bm-20260201-macm4pro-arm64-python-18347417b06d09fa7eea-3.15.0a5%2B-1834741-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.043x faster (HPT: reliability of 85.49%, 1.00x faster at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260201-macm4pro-arm64-python-18347417b06d09fa7eea-3.15.0a5%2B-1834741-vs-3.13.0rc2.md)
- [📈time plot](bm-20260201-macm4pro-arm64-python-18347417b06d09fa7eea-3.15.0a5%2B-1834741-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.052x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20260201-macm4pro-arm64-python-18347417b06d09fa7eea-3.15.0a5%2B-1834741-vs-base-mem.svg)
- [📄table](bm-20260201-macm4pro-arm64-python-18347417b06d09fa7eea-3.15.0a5%2B-1834741-vs-base.md)
- [📈time plot](bm-20260201-macm4pro-arm64-python-18347417b06d09fa7eea-3.15.0a5%2B-1834741-vs-base.svg)

