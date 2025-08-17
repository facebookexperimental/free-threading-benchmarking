# Results

- fork: python/3663b2ad54c9e15775a6
- version: 3.15.0a0
- config: 
- commit hash: [3663b2a](https://github.com/python/cpython/commit/3663b2a)
- commit date: 2025-08-16T10:29:47-04:00
- commit merge base: [5c0231c27ad2a8b85e65b4189321c128561b20b4](https://github.com/python/cpython/commit/5c0231c27ad2a8b85e65b4189321c128561b20b4)
- ref: 3663b2ad54c9e15775a6

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17014447013)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20250816-vultr-x86_64-python-3663b2ad54c9e15775a6-3.15.0a0-3663b2a-pystats.json)
- [pystats table](bm-20250816-vultr-x86_64-python-3663b2ad54c9e15775a6-3.15.0a0-3663b2a-pystats.md)
- [raw results](bm-20250816-vultr-x86_64-python-3663b2ad54c9e15775a6-3.15.0a0-3663b2a.json)

### vs. 3.12.6

- Geometric mean: 1.070x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250816-vultr-x86_64-python-3663b2ad54c9e15775a6-3.15.0a0-3663b2a-vs-3.12.6.md)
- [📈time plot](bm-20250816-vultr-x86_64-python-3663b2ad54c9e15775a6-3.15.0a0-3663b2a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.034x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250816-vultr-x86_64-python-3663b2ad54c9e15775a6-3.15.0a0-3663b2a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250816-vultr-x86_64-python-3663b2ad54c9e15775a6-3.15.0a0-3663b2a-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17014447013)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250816-macm4pro-arm64-python-3663b2ad54c9e15775a6-3.15.0a0-3663b2a.json)

### vs. 3.12.6

- Geometric mean: 1.094x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250816-macm4pro-arm64-python-3663b2ad54c9e15775a6-3.15.0a0-3663b2a-vs-3.12.6.md)
- [📈time plot](bm-20250816-macm4pro-arm64-python-3663b2ad54c9e15775a6-3.15.0a0-3663b2a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.015x faster (HPT: reliability of 80.34%, 1.00x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250816-macm4pro-arm64-python-3663b2ad54c9e15775a6-3.15.0a0-3663b2a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250816-macm4pro-arm64-python-3663b2ad54c9e15775a6-3.15.0a0-3663b2a-vs-3.13.0rc2.svg)

