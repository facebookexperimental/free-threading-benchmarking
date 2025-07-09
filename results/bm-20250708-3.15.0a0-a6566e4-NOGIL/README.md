# Results

- fork: python/a6566e49e63219b6dad6
- version: 3.15.0a0
- config: NOGIL
- commit hash: [a6566e4](https://github.com/python/cpython/commit/a6566e4)
- commit date: 2025-07-08T23:49:55+02:00
- commit merge base: [ffd7f2f231f5543e6863c6c85e86f72233229771](https://github.com/python/cpython/commit/ffd7f2f231f5543e6863c6c85e86f72233229771)
- ref: a6566e49e63219b6dad6

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16157340765)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250708-vultr-x86_64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4.json)

### vs. 3.12.6

- Geometric mean: 1.025x slower (HPT: reliability of 95.25%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250708-vultr-x86_64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.12.6.md)
- [📈time plot](bm-20250708-vultr-x86_64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.058x slower (HPT: reliability of 97.97%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250708-vultr-x86_64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.13.0rc2.md)
- [📈time plot](bm-20250708-vultr-x86_64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.094x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250708-vultr-x86_64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-base-mem.svg)
- [📄table](bm-20250708-vultr-x86_64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-base.md)
- [📈time plot](bm-20250708-vultr-x86_64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16157340765)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250708-macm4pro-arm64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4.json)

### vs. 3.12.6

- Geometric mean: 1.100x faster (HPT: reliability of 98.12%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250708-macm4pro-arm64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.12.6.md)
- [📈time plot](bm-20250708-macm4pro-arm64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.020x faster (HPT: reliability of 63.36%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250708-macm4pro-arm64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.13.0rc2.md)
- [📈time plot](bm-20250708-macm4pro-arm64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.010x slower (HPT: reliability of 97.51%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250708-macm4pro-arm64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-base-mem.svg)
- [📄table](bm-20250708-macm4pro-arm64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-base.md)
- [📈time plot](bm-20250708-macm4pro-arm64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-base.svg)

