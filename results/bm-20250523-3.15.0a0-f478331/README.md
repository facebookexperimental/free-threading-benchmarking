# Results

- fork: python/f478331f98930d94f7ef
- version: 3.15.0a0
- config: 
- commit hash: [f478331](https://github.com/python/cpython/commit/f478331)
- commit date: 2025-05-23T14:51:41-07:00
- commit merge base: [8a793c4a365d06a7264887698ccd7d6ba6aba9f2](https://github.com/python/cpython/commit/8a793c4a365d06a7264887698ccd7d6ba6aba9f2)
- ref: f478331f98930d94f7ef

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15221458727)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250523-vultr-x86_64-python-f478331f98930d94f7ef-3.15.0a0-f478331.json)

### vs. 3.12.6

- Geometric mean: 1.100x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250523-vultr-x86_64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.12.6.md)
- [📈time plot](bm-20250523-vultr-x86_64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.062x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250523-vultr-x86_64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.13.0rc2.md)
- [📈time plot](bm-20250523-vultr-x86_64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15221458727)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250523-macm4pro-arm64-python-f478331f98930d94f7ef-3.15.0a0-f478331.json)

### vs. 3.12.6

- Geometric mean: 1.127x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250523-macm4pro-arm64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.12.6.md)
- [📈time plot](bm-20250523-macm4pro-arm64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.045x faster (HPT: reliability of 99.83%, 1.00x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250523-macm4pro-arm64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.13.0rc2.md)
- [📈time plot](bm-20250523-macm4pro-arm64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.13.0rc2.svg)

