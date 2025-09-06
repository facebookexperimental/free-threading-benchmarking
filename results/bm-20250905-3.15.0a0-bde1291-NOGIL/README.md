# Results

- fork: python/bde12919522b0c40fd9e
- version: 3.15.0a0
- config: NOGIL
- commit hash: [bde1291](https://github.com/python/cpython/commit/bde1291)
- commit date: 2025-09-05T15:48:16-07:00
- commit merge base: [92b2a8a04dca506f4d2a64d68d3cc7f490a63b34](https://github.com/python/cpython/commit/92b2a8a04dca506f4d2a64d68d3cc7f490a63b34)
- ref: bde12919522b0c40fd9e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17507375969)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250905-vultr-x86_64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291.json)

### vs. 3.12.6

- Geometric mean: 1.022x slower (HPT: reliability of 85.65%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250905-vultr-x86_64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291-vs-3.12.6.md)
- [📈time plot](bm-20250905-vultr-x86_64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x slower (HPT: reliability of 97.80%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250905-vultr-x86_64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291-vs-3.13.0rc2.md)
- [📈time plot](bm-20250905-vultr-x86_64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.094x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20250905-vultr-x86_64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291-vs-base-mem.svg)
- [📄table](bm-20250905-vultr-x86_64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291-vs-base.md)
- [📈time plot](bm-20250905-vultr-x86_64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17507375969)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291.json)

### vs. 3.12.6

- Geometric mean: 1.087x faster (HPT: reliability of 97.30%, 1.00x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291-vs-3.12.6.md)
- [📈time plot](bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.009x faster (HPT: reliability of 66.26%, 1.00x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291-vs-3.13.0rc2.md)
- [📈time plot](bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.022x slower (HPT: reliability of 99.34%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291-vs-base-mem.svg)
- [📄table](bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291-vs-base.md)
- [📈time plot](bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291-vs-base.svg)

