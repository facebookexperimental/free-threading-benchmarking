# Results

- fork: python/95d6e0b2830c8e6bfd86
- version: 3.15.0a0
- config: 
- commit hash: [95d6e0b](https://github.com/python/cpython/commit/95d6e0b)
- commit date: 2025-08-25T21:59:52+01:00
- commit merge base: [9ee0214b5dd982ac9fbe18dcce0e8787456e29af](https://github.com/python/cpython/commit/9ee0214b5dd982ac9fbe18dcce0e8787456e29af)
- ref: 95d6e0b2830c8e6bfd86

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17224312467)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250825-vultr-x86_64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b.json)

### vs. 3.12.6

- Geometric mean: 1.070x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250825-vultr-x86_64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b-vs-3.12.6.md)
- [📈time plot](bm-20250825-vultr-x86_64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.034x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250825-vultr-x86_64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250825-vultr-x86_64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17224312467)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b.json)

### vs. 3.12.6

- Geometric mean: 1.111x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b-vs-3.12.6.md)
- [📈time plot](bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.031x faster (HPT: reliability of 97.52%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250825-macm4pro-arm64-python-95d6e0b2830c8e6bfd86-3.15.0a0-95d6e0b-vs-3.13.0rc2.svg)

