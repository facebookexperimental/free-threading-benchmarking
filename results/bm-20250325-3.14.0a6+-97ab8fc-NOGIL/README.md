# Results

- fork: python/97ab8fc16a8e0b0e2e68
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [97ab8fc](https://github.com/python/cpython/commit/97ab8fc)
- commit date: 2025-03-25T05:43:31+08:00
- commit merge base: [a1232459860235f4fb7896cc95966d87a51cbe32](https://github.com/python/cpython/commit/a1232459860235f4fb7896cc95966d87a51cbe32)
- ref: 97ab8fc16a8e0b0e2e68

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14065299425)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250325-vultr-x86_64-python-97ab8fc16a8e0b0e2e68-3.14.0a6%2B-97ab8fc.json)

### vs. 3.12.6

- Geometric mean: 1.044x slower (HPT: reliability of 99.99%, 1.02x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250325-vultr-x86_64-python-97ab8fc16a8e0b0e2e68-3.14.0a6%2B-97ab8fc-vs-3.12.6.md)
- [📈time plot](bm-20250325-vultr-x86_64-python-97ab8fc16a8e0b0e2e68-3.14.0a6%2B-97ab8fc-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.076x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250325-vultr-x86_64-python-97ab8fc16a8e0b0e2e68-3.14.0a6%2B-97ab8fc-vs-3.13.0rc2.md)
- [📈time plot](bm-20250325-vultr-x86_64-python-97ab8fc16a8e0b0e2e68-3.14.0a6%2B-97ab8fc-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.110x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.21x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250325-vultr-x86_64-python-97ab8fc16a8e0b0e2e68-3.14.0a6%2B-97ab8fc-vs-base-mem.svg)
- [📄table](bm-20250325-vultr-x86_64-python-97ab8fc16a8e0b0e2e68-3.14.0a6%2B-97ab8fc-vs-base.md)
- [📈time plot](bm-20250325-vultr-x86_64-python-97ab8fc16a8e0b0e2e68-3.14.0a6%2B-97ab8fc-vs-base.svg)

