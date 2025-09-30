# Results

- fork: python/6b5f15698a436591f7c3
- version: 3.15.0a0
- config: 
- commit hash: [6b5f156](https://github.com/python/cpython/commit/6b5f156)
- commit date: 2025-09-29T18:59:25+01:00
- commit merge base: [1b8dcdacc75caa8175f89c7e739e45d856ebf511](https://github.com/python/cpython/commit/1b8dcdacc75caa8175f89c7e739e45d856ebf511)
- ref: 6b5f15698a436591f7c3

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18114629382)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250929-vultr-x86_64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156.json)

### vs. 3.12.6

- Geometric mean: 1.073x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250929-vultr-x86_64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.12.6.md)
- [📈time plot](bm-20250929-vultr-x86_64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.037x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250929-vultr-x86_64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.13.0rc2.md)
- [📈time plot](bm-20250929-vultr-x86_64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18114629382)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250929-macm4pro-arm64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156.json)

### vs. 3.12.6

- Geometric mean: 1.087x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250929-macm4pro-arm64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.12.6.md)
- [📈time plot](bm-20250929-macm4pro-arm64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.008x faster (HPT: reliability of 54.29%, 1.00x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250929-macm4pro-arm64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.13.0rc2.md)
- [📈time plot](bm-20250929-macm4pro-arm64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.13.0rc2.svg)

