# Results

- fork: Yhg1s/cell_critsect
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [e9fdced](https://github.com/Yhg1s/cpython/commit/e9fdced)
- commit date: 2025-03-28T15:29:10+01:00
- commit merge base: [898e6b395e63ad7f8bbe421adf0af8947d429925](https://github.com/python/cpython/commit/898e6b395e63ad7f8bbe421adf0af8947d429925)
- ref: cell_critsect

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14130956766)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6%2B-e9fdced.json)

### vs. 3.12.6

- Geometric mean: 1.045x slower (HPT: reliability of 99.99%, 1.02x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6%2B-e9fdced-vs-3.12.6.md)
- [📈time plot](bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6%2B-e9fdced-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.076x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6%2B-e9fdced-vs-3.13.0rc2.md)
- [📈time plot](bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6%2B-e9fdced-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x faster (HPT: reliability of 95.10%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6%2B-e9fdced-vs-base-mem.svg)
- [📄table](bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6%2B-e9fdced-vs-base.md)
- [📈time plot](bm-20250328-vultr-x86_64-Yhg1s-cell_critsect-3.14.0a6%2B-e9fdced-vs-base.svg)

