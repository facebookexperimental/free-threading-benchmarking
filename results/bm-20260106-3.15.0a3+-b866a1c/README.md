# Results

- fork: python/b866a1c73f8160647545
- version: 3.15.0a3+
- config: 
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

- Geometric mean: 1.069x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260106-vultr-x86_64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c-vs-3.12.6.md)
- [📈time plot](bm-20260106-vultr-x86_64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.033x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260106-vultr-x86_64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c-vs-3.13.0rc2.md)
- [📈time plot](bm-20260106-vultr-x86_64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20766514041)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260106-macm4pro-arm64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c.json)

### vs. 3.12.6

- Geometric mean: 1.159x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260106-macm4pro-arm64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c-vs-3.12.6.md)
- [📈time plot](bm-20260106-macm4pro-arm64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260106-macm4pro-arm64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c-vs-3.13.0rc2.md)
- [📈time plot](bm-20260106-macm4pro-arm64-python-b866a1c73f8160647545-3.15.0a3%2B-b866a1c-vs-3.13.0rc2.svg)

