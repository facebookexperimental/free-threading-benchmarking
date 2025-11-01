# Results

- fork: python/a17c57eee5b5cc813907
- version: 3.15.0a1+
- config: 
- commit hash: [a17c57e](https://github.com/python/cpython/commit/a17c57e)
- commit date: 2025-10-31T17:44:02+02:00
- commit merge base: [07912f86323dc5a13f4d070b7e3f2c3cb2850d8b](https://github.com/python/cpython/commit/07912f86323dc5a13f4d070b7e3f2c3cb2850d8b)
- ref: a17c57eee5b5cc813907

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18988488906)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251031-vultr-x86_64-python-a17c57eee5b5cc813907-3.15.0a1%2B-a17c57e.json)

### vs. 3.12.6

- Geometric mean: 1.078x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251031-vultr-x86_64-python-a17c57eee5b5cc813907-3.15.0a1%2B-a17c57e-vs-3.12.6.md)
- [📈time plot](bm-20251031-vultr-x86_64-python-a17c57eee5b5cc813907-3.15.0a1%2B-a17c57e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.042x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251031-vultr-x86_64-python-a17c57eee5b5cc813907-3.15.0a1%2B-a17c57e-vs-3.13.0rc2.md)
- [📈time plot](bm-20251031-vultr-x86_64-python-a17c57eee5b5cc813907-3.15.0a1%2B-a17c57e-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18988488906)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251031-macm4pro-arm64-python-a17c57eee5b5cc813907-3.15.0a1%2B-a17c57e.json)

### vs. 3.12.6

- Geometric mean: 1.104x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251031-macm4pro-arm64-python-a17c57eee5b5cc813907-3.15.0a1%2B-a17c57e-vs-3.12.6.md)
- [📈time plot](bm-20251031-macm4pro-arm64-python-a17c57eee5b5cc813907-3.15.0a1%2B-a17c57e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.024x faster (HPT: reliability of 79.19%, 1.00x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251031-macm4pro-arm64-python-a17c57eee5b5cc813907-3.15.0a1%2B-a17c57e-vs-3.13.0rc2.md)
- [📈time plot](bm-20251031-macm4pro-arm64-python-a17c57eee5b5cc813907-3.15.0a1%2B-a17c57e-vs-3.13.0rc2.svg)

