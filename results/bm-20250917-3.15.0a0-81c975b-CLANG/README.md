# Results

- fork: python/81c975bcfc1ac0533f94
- version: 3.15.0a0
- config: CLANG
- commit hash: [81c975b](https://github.com/python/cpython/commit/81c975b)
- commit date: 2025-09-17T21:45:34+08:00
- commit merge base: [5df6a568e172e45933d1cb26f90e6e57b4bbe0a6](https://github.com/python/cpython/commit/5df6a568e172e45933d1cb26f90e6e57b4bbe0a6)
- ref: 81c975bcfc1ac0533f94

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17813555614)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250917-vultr-x86_64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b.json)

### vs. 3.12.6

- Geometric mean: 1.121x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250917-vultr-x86_64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b-vs-3.12.6.md)
- [📈time plot](bm-20250917-vultr-x86_64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.084x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250917-vultr-x86_64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250917-vultr-x86_64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17813555614)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250917-macm4pro-arm64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b.json)

### vs. 3.12.6

- Geometric mean: 1.145x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250917-macm4pro-arm64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b-vs-3.12.6.md)
- [📈time plot](bm-20250917-macm4pro-arm64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.062x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250917-macm4pro-arm64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250917-macm4pro-arm64-python-81c975bcfc1ac0533f94-3.15.0a0-81c975b-vs-3.13.0rc2.svg)

