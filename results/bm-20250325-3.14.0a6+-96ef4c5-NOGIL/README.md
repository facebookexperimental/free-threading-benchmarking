# Results

- fork: python/96ef4c511f3ec763dbb0
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [96ef4c5](https://github.com/python/cpython/commit/96ef4c5)
- commit date: 2025-03-25T16:48:46+05:30
- commit merge base: [6fb5f7f4d9d22c49f5c29d2ffcbcc32b6cd7d06a](https://github.com/python/cpython/commit/6fb5f7f4d9d22c49f5c29d2ffcbcc32b6cd7d06a)
- ref: 96ef4c511f3ec763dbb0

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14264982634)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6%2B-96ef4c5.json)

### vs. 3.12.6

- Geometric mean: 1.042x slower (HPT: reliability of 99.99%, 1.02x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6%2B-96ef4c5-vs-3.12.6.md)
- [📈time plot](bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6%2B-96ef4c5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.074x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6%2B-96ef4c5-vs-3.13.0rc2.md)
- [📈time plot](bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6%2B-96ef4c5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.111x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.21x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6%2B-96ef4c5-vs-base-mem.svg)
- [📄table](bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6%2B-96ef4c5-vs-base.md)
- [📈time plot](bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6%2B-96ef4c5-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14264979175)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6%2B-96ef4c5.json)

### vs. 3.12.6

- Geometric mean: 1.049x faster (HPT: reliability of 54.65%, 1.00x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6%2B-96ef4c5-vs-3.12.6.md)
- [📈time plot](bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6%2B-96ef4c5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.027x slower (HPT: reliability of 97.91%, 1.00x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6%2B-96ef4c5-vs-3.13.0rc2.md)
- [📈time plot](bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6%2B-96ef4c5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.017x slower (HPT: reliability of 99.79%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6%2B-96ef4c5-vs-base-mem.svg)
- [📄table](bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6%2B-96ef4c5-vs-base.md)
- [📈time plot](bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6%2B-96ef4c5-vs-base.svg)

