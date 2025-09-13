# Results

- fork: python/805e3368d6d07e584306
- version: 3.15.0a0
- config: 
- commit hash: [805e336](https://github.com/python/cpython/commit/805e336)
- commit date: 2025-09-12T22:25:18+01:00
- commit merge base: [2e8f64c9317a327a2be1ab8031844ef3967c1040](https://github.com/python/cpython/commit/2e8f64c9317a327a2be1ab8031844ef3967c1040)
- ref: 805e3368d6d07e584306

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17688988932)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250912-vultr-x86_64-python-805e3368d6d07e584306-3.15.0a0-805e336.json)

### vs. 3.12.6

- Geometric mean: 1.067x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250912-vultr-x86_64-python-805e3368d6d07e584306-3.15.0a0-805e336-vs-3.12.6.md)
- [📈time plot](bm-20250912-vultr-x86_64-python-805e3368d6d07e584306-3.15.0a0-805e336-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.032x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250912-vultr-x86_64-python-805e3368d6d07e584306-3.15.0a0-805e336-vs-3.13.0rc2.md)
- [📈time plot](bm-20250912-vultr-x86_64-python-805e3368d6d07e584306-3.15.0a0-805e336-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17688988932)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250912-macm4pro-arm64-python-805e3368d6d07e584306-3.15.0a0-805e336.json)

### vs. 3.12.6

- Geometric mean: 1.110x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250912-macm4pro-arm64-python-805e3368d6d07e584306-3.15.0a0-805e336-vs-3.12.6.md)
- [📈time plot](bm-20250912-macm4pro-arm64-python-805e3368d6d07e584306-3.15.0a0-805e336-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.030x faster (HPT: reliability of 93.31%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250912-macm4pro-arm64-python-805e3368d6d07e584306-3.15.0a0-805e336-vs-3.13.0rc2.md)
- [📈time plot](bm-20250912-macm4pro-arm64-python-805e3368d6d07e584306-3.15.0a0-805e336-vs-3.13.0rc2.svg)

