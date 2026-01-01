# Results

- fork: python/c5215978ebfea9471f31
- version: 3.15.0a3+
- config: NOGIL
- commit hash: [c521597](https://github.com/python/cpython/commit/c521597)
- commit date: 2025-12-31T21:45:41+01:00
- commit merge base: [3c4429f65a894af2a0aea2aeed5f61bc399e5af5](https://github.com/python/cpython/commit/3c4429f65a894af2a0aea2aeed5f61bc399e5af5)
- ref: c5215978ebfea9471f31

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20629836204)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251231-vultr-x86_64-python-c5215978ebfea9471f31-3.15.0a3%2B-c521597.json)

### vs. 3.12.6

- Geometric mean: 1.031x slower (HPT: reliability of 84.65%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251231-vultr-x86_64-python-c5215978ebfea9471f31-3.15.0a3%2B-c521597-vs-3.12.6.md)
- [📈time plot](bm-20251231-vultr-x86_64-python-c5215978ebfea9471f31-3.15.0a3%2B-c521597-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.064x slower (HPT: reliability of 95.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251231-vultr-x86_64-python-c5215978ebfea9471f31-3.15.0a3%2B-c521597-vs-3.13.0rc2.md)
- [📈time plot](bm-20251231-vultr-x86_64-python-c5215978ebfea9471f31-3.15.0a3%2B-c521597-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.100x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20251231-vultr-x86_64-python-c5215978ebfea9471f31-3.15.0a3%2B-c521597-vs-base-mem.svg)
- [📄table](bm-20251231-vultr-x86_64-python-c5215978ebfea9471f31-3.15.0a3%2B-c521597-vs-base.md)
- [📈time plot](bm-20251231-vultr-x86_64-python-c5215978ebfea9471f31-3.15.0a3%2B-c521597-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20629836204)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251231-macm4pro-arm64-python-c5215978ebfea9471f31-3.15.0a3%2B-c521597.json)

### vs. 3.12.6

- Geometric mean: 1.111x faster (HPT: reliability of 99.71%, 1.01x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251231-macm4pro-arm64-python-c5215978ebfea9471f31-3.15.0a3%2B-c521597-vs-3.12.6.md)
- [📈time plot](bm-20251231-macm4pro-arm64-python-c5215978ebfea9471f31-3.15.0a3%2B-c521597-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.029x faster (HPT: reliability of 60.79%, 1.00x faster at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251231-macm4pro-arm64-python-c5215978ebfea9471f31-3.15.0a3%2B-c521597-vs-3.13.0rc2.md)
- [📈time plot](bm-20251231-macm4pro-arm64-python-c5215978ebfea9471f31-3.15.0a3%2B-c521597-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.065x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: 🔴 asyncio_websockets
- [🧠memory plot](bm-20251231-macm4pro-arm64-python-c5215978ebfea9471f31-3.15.0a3%2B-c521597-vs-base-mem.svg)
- [📄table](bm-20251231-macm4pro-arm64-python-c5215978ebfea9471f31-3.15.0a3%2B-c521597-vs-base.md)
- [📈time plot](bm-20251231-macm4pro-arm64-python-c5215978ebfea9471f31-3.15.0a3%2B-c521597-vs-base.svg)

