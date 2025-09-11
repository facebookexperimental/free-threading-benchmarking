# Results

- fork: python/d0c9943869bb143df445
- version: 3.15.0a0
- config: NOGIL
- commit hash: [d0c9943](https://github.com/python/cpython/commit/d0c9943)
- commit date: 2025-09-10T15:52:57Z
- commit merge base: [6e78a539bfb406238ec251ba01b7a1819e5c303e](https://github.com/python/cpython/commit/6e78a539bfb406238ec251ba01b7a1819e5c303e)
- commit date: 2025-09-10T15:52:57+00:00
- ref: d0c9943869bb143df445

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17630298084)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250910-vultr-x86_64-python-d0c9943869bb143df445-3.15.0a0-d0c9943.json)

### vs. 3.12.6

- Geometric mean: 1.018x slower (HPT: reliability of 85.97%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250910-vultr-x86_64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.12.6.md)
- [📈time plot](bm-20250910-vultr-x86_64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.051x slower (HPT: reliability of 95.75%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250910-vultr-x86_64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.13.0rc2.md)
- [📈time plot](bm-20250910-vultr-x86_64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.084x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20250910-vultr-x86_64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-base-mem.svg)
- [📄table](bm-20250910-vultr-x86_64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-base.md)
- [📈time plot](bm-20250910-vultr-x86_64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17630298084)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250910-macm4pro-arm64-python-d0c9943869bb143df445-3.15.0a0-d0c9943.json)

### vs. 3.12.6

- Geometric mean: 1.073x faster (HPT: reliability of 90.18%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250910-macm4pro-arm64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.12.6.md)
- [📈time plot](bm-20250910-macm4pro-arm64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.004x slower (HPT: reliability of 85.41%, 1.00x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250910-macm4pro-arm64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.13.0rc2.md)
- [📈time plot](bm-20250910-macm4pro-arm64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.022x slower (HPT: reliability of 99.76%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20250910-macm4pro-arm64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-base-mem.svg)
- [📄table](bm-20250910-macm4pro-arm64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-base.md)
- [📈time plot](bm-20250910-macm4pro-arm64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-base.svg)

