# Results

- fork: python/main
- version: 3.15.0a2+
- config: JIT
- commit hash: [dc62b62](https://github.com/python/cpython/commit/dc62b62)
- commit date: 2025-11-24T22:07:45Z
- commit merge base: [369ce2b139a5b76c9c093cba1cee287cb6ffeec1](https://github.com/python/cpython/commit/369ce2b139a5b76c9c093cba1cee287cb6ffeec1)
- fork: python/dc62b622524bf49eb539
- commit date: 2025-11-24T22:07:45+00:00
- ref: dc62b622524bf49eb539, main

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19653626709)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19651864805)
- [raw results](bm-20251124-vultr-x86_64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62.json)
- [raw results](bm-20251124-vultr-x86_64-python-main-3.15.0a2%2B-dc62b62.json)

### vs. 3.12.6

- Geometric mean: 1.102x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20251124-vultr-x86_64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-3.12.6.md)
- [📈time plot](bm-20251124-vultr-x86_64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-3.12.6.svg)
- [📄table](bm-20251124-vultr-x86_64-python-main-3.15.0a2%2B-dc62b62-vs-3.12.6.md)
- [📈time plot](bm-20251124-vultr-x86_64-python-main-3.15.0a2%2B-dc62b62-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.064x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- Geometric mean: 1.065x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20251124-vultr-x86_64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-3.13.0rc2.md)
- [📈time plot](bm-20251124-vultr-x86_64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-3.13.0rc2.svg)
- [📄table](bm-20251124-vultr-x86_64-python-main-3.15.0a2%2B-dc62b62-vs-3.13.0rc2.md)
- [📈time plot](bm-20251124-vultr-x86_64-python-main-3.15.0a2%2B-dc62b62-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x faster (HPT: reliability of 76.99%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- new benchmarks: docutils
- Geometric mean: 1.001x faster (HPT: reliability of 95.69%, 1.00x slower at 99th %ile)
- [🧠memory plot](bm-20251124-vultr-x86_64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-base-mem.svg)
- [📄table](bm-20251124-vultr-x86_64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-base.md)
- [📈time plot](bm-20251124-vultr-x86_64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-base.svg)
- [🧠memory plot](bm-20251124-vultr-x86_64-python-main-3.15.0a2%2B-dc62b62-vs-base-mem.svg)
- [📄table](bm-20251124-vultr-x86_64-python-main-3.15.0a2%2B-dc62b62-vs-base.md)
- [📈time plot](bm-20251124-vultr-x86_64-python-main-3.15.0a2%2B-dc62b62-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19653626709)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19651864805)
- [raw results](bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62.json)
- [raw results](bm-20251124-macm4pro-arm64-python-main-3.15.0a2%2B-dc62b62.json)

### vs. 3.12.6

- Geometric mean: 1.166x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, connected_components, dask, djangocms, docutils, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- Geometric mean: 1.165x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: chameleon, connected_components, djangocms, docutils, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- [📄table](bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-3.12.6.md)
- [📈time plot](bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-3.12.6.svg)
- [📄table](bm-20251124-macm4pro-arm64-python-main-3.15.0a2%2B-dc62b62-vs-3.12.6.md)
- [📈time plot](bm-20251124-macm4pro-arm64-python-main-3.15.0a2%2B-dc62b62-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.073x faster (HPT: reliability of 96.35%, 1.00x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, connected_components, dask, djangocms, docutils, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- Geometric mean: 1.073x faster (HPT: reliability of 93.96%, 1.00x faster at 99th %ile)
- missing benchmarks: chameleon, connected_components, djangocms, docutils, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- [📄table](bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-3.13.0rc2.md)
- [📈time plot](bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-3.13.0rc2.svg)
- [📄table](bm-20251124-macm4pro-arm64-python-main-3.15.0a2%2B-dc62b62-vs-3.13.0rc2.md)
- [📈time plot](bm-20251124-macm4pro-arm64-python-main-3.15.0a2%2B-dc62b62-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x slower (HPT: reliability of 99.96%, 1.00x slower at 99th %ile)
- Memory usage: 0.98x
- missing benchmarks: 🔴 dask
- Geometric mean: 1.002x slower (HPT: reliability of 56.92%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-base-mem.svg)
- [📄table](bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-base.md)
- [📈time plot](bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-base.svg)
- [🧠memory plot](bm-20251124-macm4pro-arm64-python-main-3.15.0a2%2B-dc62b62-vs-base-mem.svg)
- [📄table](bm-20251124-macm4pro-arm64-python-main-3.15.0a2%2B-dc62b62-vs-base.md)
- [📈time plot](bm-20251124-macm4pro-arm64-python-main-3.15.0a2%2B-dc62b62-vs-base.svg)

