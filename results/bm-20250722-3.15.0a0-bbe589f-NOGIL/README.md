# Results

- fork: python/bbe589f93ccaf32eb95f
- version: 3.15.0a0
- config: NOGIL
- commit hash: [bbe589f](https://github.com/python/cpython/commit/bbe589f)
- commit date: 2025-07-22T07:58:31+08:00
- commit merge base: [6bf1c0ab3497b1b193812654bcdfd0c11b4192d8](https://github.com/python/cpython/commit/6bf1c0ab3497b1b193812654bcdfd0c11b4192d8)
- ref: bbe589f93ccaf32eb95f

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16431382835)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json)

### vs. 3.12.6

- Geometric mean: 1.023x slower (HPT: reliability of 94.16%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f-vs-3.12.6.md)
- [📈time plot](bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.056x slower (HPT: reliability of 97.12%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.095x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f-vs-base-mem.svg)
- [📄table](bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f-vs-base.md)
- [📈time plot](bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16431382835)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json)

### vs. 3.12.6

- Geometric mean: 1.082x faster (HPT: reliability of 94.92%, 1.00x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f-vs-3.12.6.md)
- [📈time plot](bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.003x faster (HPT: reliability of 76.20%, 1.00x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.010x slower (HPT: reliability of 93.68%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f-vs-base-mem.svg)
- [📄table](bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f-vs-base.md)
- [📈time plot](bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f-vs-base.svg)

