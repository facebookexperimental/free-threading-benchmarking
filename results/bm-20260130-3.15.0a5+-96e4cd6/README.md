# Results

- fork: python/96e4cd698a3000382f17
- version: 3.15.0a5+
- config: 
- commit hash: [96e4cd6](https://github.com/python/cpython/commit/96e4cd6)
- commit date: 2026-01-30T18:18:56Z
- commit merge base: [a01694dacd8e8bbbd019e8b87dbc7bc7173cb7f1](https://github.com/python/cpython/commit/a01694dacd8e8bbbd019e8b87dbc7bc7173cb7f1)
- commit date: 2026-01-30T18:18:56+00:00
- ref: 96e4cd698a3000382f17

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21535507618)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260130-vultr-x86_64-python-96e4cd698a3000382f17-3.15.0a5%2B-96e4cd6.json)

### vs. 3.12.6

- Geometric mean: 1.074x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260130-vultr-x86_64-python-96e4cd698a3000382f17-3.15.0a5%2B-96e4cd6-vs-3.12.6.md)
- [📈time plot](bm-20260130-vultr-x86_64-python-96e4cd698a3000382f17-3.15.0a5%2B-96e4cd6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.038x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260130-vultr-x86_64-python-96e4cd698a3000382f17-3.15.0a5%2B-96e4cd6-vs-3.13.0rc2.md)
- [📈time plot](bm-20260130-vultr-x86_64-python-96e4cd698a3000382f17-3.15.0a5%2B-96e4cd6-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21535507618)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5%2B-96e4cd6.json)

### vs. 3.12.6

- Geometric mean: 1.198x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5%2B-96e4cd6-vs-3.12.6.md)
- [📈time plot](bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5%2B-96e4cd6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.111x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5%2B-96e4cd6-vs-3.13.0rc2.md)
- [📈time plot](bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5%2B-96e4cd6-vs-3.13.0rc2.svg)

