# Results

- fork: python/645f5c4a737b3eab29d0
- version: 3.15.0a6+
- config: NOGIL
- commit hash: [645f5c4](https://github.com/python/cpython/commit/645f5c4)
- commit date: 2026-02-14T19:20:33Z
- commit merge base: [caac966b0051578b60b4b07fe341174f25d9f8b1](https://github.com/python/cpython/commit/caac966b0051578b60b4b07fe341174f25d9f8b1)
- commit date: 2026-02-14T19:20:33+00:00
- ref: 645f5c4a737b3eab29d0

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22026694395)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260214-vultr-x86_64-python-645f5c4a737b3eab29d0-3.15.0a6%2B-645f5c4.json)

### vs. 3.12.6

- Geometric mean: 1.034x slower (HPT: reliability of 80.47%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260214-vultr-x86_64-python-645f5c4a737b3eab29d0-3.15.0a6%2B-645f5c4-vs-3.12.6.md)
- [📈time plot](bm-20260214-vultr-x86_64-python-645f5c4a737b3eab29d0-3.15.0a6%2B-645f5c4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.067x slower (HPT: reliability of 94.70%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260214-vultr-x86_64-python-645f5c4a737b3eab29d0-3.15.0a6%2B-645f5c4-vs-3.13.0rc2.md)
- [📈time plot](bm-20260214-vultr-x86_64-python-645f5c4a737b3eab29d0-3.15.0a6%2B-645f5c4-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.109x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260214-vultr-x86_64-python-645f5c4a737b3eab29d0-3.15.0a6%2B-645f5c4-vs-base-mem.svg)
- [📄table](bm-20260214-vultr-x86_64-python-645f5c4a737b3eab29d0-3.15.0a6%2B-645f5c4-vs-base.md)
- [📈time plot](bm-20260214-vultr-x86_64-python-645f5c4a737b3eab29d0-3.15.0a6%2B-645f5c4-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22026694395)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6%2B-645f5c4.json)

### vs. 3.12.6

- Geometric mean: 1.102x faster (HPT: reliability of 99.97%, 1.01x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6%2B-645f5c4-vs-3.12.6.md)
- [📈time plot](bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6%2B-645f5c4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.023x faster (HPT: reliability of 70.22%, 1.00x faster at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6%2B-645f5c4-vs-3.13.0rc2.md)
- [📈time plot](bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6%2B-645f5c4-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.056x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6%2B-645f5c4-vs-base-mem.svg)
- [📄table](bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6%2B-645f5c4-vs-base.md)
- [📈time plot](bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6%2B-645f5c4-vs-base.svg)

