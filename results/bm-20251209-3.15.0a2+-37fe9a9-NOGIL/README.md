# Results

- fork: python/37fe9a90c5f99fd3830b
- version: 3.15.0a2+
- config: NOGIL
- commit hash: [37fe9a9](https://github.com/python/cpython/commit/37fe9a9)
- commit date: 2025-12-09T23:07:50+00:00
- commit merge base: [91884838bc3c47e02ab6099e6f9b12d80a0abae2](https://github.com/python/cpython/commit/91884838bc3c47e02ab6099e6f9b12d80a0abae2)
- ref: 37fe9a90c5f99fd3830b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20083070235)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251209-vultr-x86_64-python-37fe9a90c5f99fd3830b-3.15.0a2%2B-37fe9a9.json)

### vs. 3.12.6

- Geometric mean: 1.038x slower (HPT: reliability of 90.64%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251209-vultr-x86_64-python-37fe9a90c5f99fd3830b-3.15.0a2%2B-37fe9a9-vs-3.12.6.md)
- [📈time plot](bm-20251209-vultr-x86_64-python-37fe9a90c5f99fd3830b-3.15.0a2%2B-37fe9a9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.070x slower (HPT: reliability of 99.19%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251209-vultr-x86_64-python-37fe9a90c5f99fd3830b-3.15.0a2%2B-37fe9a9-vs-3.13.0rc2.md)
- [📈time plot](bm-20251209-vultr-x86_64-python-37fe9a90c5f99fd3830b-3.15.0a2%2B-37fe9a9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.109x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20251209-vultr-x86_64-python-37fe9a90c5f99fd3830b-3.15.0a2%2B-37fe9a9-vs-base-mem.svg)
- [📄table](bm-20251209-vultr-x86_64-python-37fe9a90c5f99fd3830b-3.15.0a2%2B-37fe9a9-vs-base.md)
- [📈time plot](bm-20251209-vultr-x86_64-python-37fe9a90c5f99fd3830b-3.15.0a2%2B-37fe9a9-vs-base.svg)

