# Results

- fork: python/b866a1c73f8160647545
- version: 3.15.0a3+
- config: NOGIL
- commit hash: [b866a1c](https://github.com/python/cpython/commit/b866a1c)
- commit date: 2026-01-06T23:51:12Z
- commit merge base: [4fb6a31bce36c8e04c0bda63f13467fc594b4425](https://github.com/python/cpython/commit/4fb6a31bce36c8e04c0bda63f13467fc594b4425)
- commit date: 2026-01-06T23:51:12+00:00
- ref: b866a1c73f8160647545

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20766514041)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260106-vultr-x86_64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c.json)

### vs. 3.12.6

- Geometric mean: 1.030x slower (HPT: reliability of 74.75%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260106-vultr-x86_64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c-vs-3.12.6.md)
- [📈time plot](bm-20260106-vultr-x86_64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.063x slower (HPT: reliability of 89.38%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260106-vultr-x86_64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c-vs-3.13.0rc2.md)
- [📈time plot](bm-20260106-vultr-x86_64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.097x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20260106-vultr-x86_64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c-vs-base-mem.svg)
- [📄table](bm-20260106-vultr-x86_64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c-vs-base.md)
- [📈time plot](bm-20260106-vultr-x86_64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20766514041)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260106-macm4pro-arm64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c.json)

### vs. 3.12.6

- Geometric mean: 1.082x faster (HPT: reliability of 97.56%, 1.00x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260106-macm4pro-arm64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c-vs-3.12.6.md)
- [📈time plot](bm-20260106-macm4pro-arm64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.004x faster (HPT: reliability of 77.78%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260106-macm4pro-arm64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c-vs-3.13.0rc2.md)
- [📈time plot](bm-20260106-macm4pro-arm64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.067x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20260106-macm4pro-arm64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c-vs-base-mem.svg)
- [📄table](bm-20260106-macm4pro-arm64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c-vs-base.md)
- [📈time plot](bm-20260106-macm4pro-arm64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c-vs-base.svg)

