# Results

- fork: python/52be7f445e454ccb44e3
- version: 3.15.0a0
- config: 
- commit hash: [52be7f4](https://github.com/python/cpython/commit/52be7f4)
- commit date: 2025-06-18T08:36:02+09:00
- commit merge base: [cb394101110e13a27e08bbf2fe9f38d847db004c](https://github.com/python/cpython/commit/cb394101110e13a27e08bbf2fe9f38d847db004c)
- ref: 52be7f445e454ccb44e3

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15720939817)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250618-vultr-x86_64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4.json)

### vs. 3.12.6

- Geometric mean: 1.110x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250618-vultr-x86_64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.12.6.md)
- [📈time plot](bm-20250618-vultr-x86_64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.072x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250618-vultr-x86_64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.13.0rc2.md)
- [📈time plot](bm-20250618-vultr-x86_64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15720939817)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4.json)

### vs. 3.12.6

- Geometric mean: 1.102x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.12.6.md)
- [📈time plot](bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.022x faster (HPT: reliability of 69.18%, 1.00x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.13.0rc2.md)
- [📈time plot](bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.13.0rc2.svg)

