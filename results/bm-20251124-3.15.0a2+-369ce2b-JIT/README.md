# Results

- fork: python/369ce2b139a5b76c9c09
- version: 3.15.0a2+
- config: JIT
- commit hash: [369ce2b](https://github.com/python/cpython/commit/369ce2b)
- commit date: 2025-11-24T14:48:28-05:00
- commit merge base: [fee778265064c290ae1852916ff47fcc0ab4a29d](https://github.com/python/cpython/commit/fee778265064c290ae1852916ff47fcc0ab4a29d)
- ref: 369ce2b139a5b76c9c09

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19653626709)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251124-vultr-x86_64-python-369ce2b139a5b76c9c09-3.15.0a2%2B-369ce2b.json)

### vs. 3.12.6

- Geometric mean: 1.101x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251124-vultr-x86_64-python-369ce2b139a5b76c9c09-3.15.0a2%2B-369ce2b-vs-3.12.6.md)
- [📈time plot](bm-20251124-vultr-x86_64-python-369ce2b139a5b76c9c09-3.15.0a2%2B-369ce2b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.064x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251124-vultr-x86_64-python-369ce2b139a5b76c9c09-3.15.0a2%2B-369ce2b-vs-3.13.0rc2.md)
- [📈time plot](bm-20251124-vultr-x86_64-python-369ce2b139a5b76c9c09-3.15.0a2%2B-369ce2b-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19653626709)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251124-macm4pro-arm64-python-369ce2b139a5b76c9c09-3.15.0a2%2B-369ce2b.json)

### vs. 3.12.6

- Geometric mean: 1.166x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: chameleon, connected_components, djangocms, docutils, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251124-macm4pro-arm64-python-369ce2b139a5b76c9c09-3.15.0a2%2B-369ce2b-vs-3.12.6.md)
- [📈time plot](bm-20251124-macm4pro-arm64-python-369ce2b139a5b76c9c09-3.15.0a2%2B-369ce2b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.074x faster (HPT: reliability of 94.01%, 1.00x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, connected_components, djangocms, docutils, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251124-macm4pro-arm64-python-369ce2b139a5b76c9c09-3.15.0a2%2B-369ce2b-vs-3.13.0rc2.md)
- [📈time plot](bm-20251124-macm4pro-arm64-python-369ce2b139a5b76c9c09-3.15.0a2%2B-369ce2b-vs-3.13.0rc2.svg)

