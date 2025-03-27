# Results

- fork: Yhg1s/avoid_list_critsect
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [e69e45f](https://github.com/Yhg1s/cpython/commit/e69e45f)
- commit date: 2025-03-27T15:35:33+01:00
- commit merge base: [898e6b395e63ad7f8bbe421adf0af8947d429925](https://github.com/python/cpython/commit/898e6b395e63ad7f8bbe421adf0af8947d429925)
- ref: avoid_list_critsect

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14109447051)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6%2B-e69e45f.json)

### vs. 3.12.6

- Geometric mean: 1.050x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6%2B-e69e45f-vs-3.12.6.md)
- [📈time plot](bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6%2B-e69e45f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.082x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6%2B-e69e45f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6%2B-e69e45f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x slower (HPT: reliability of 98.33%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6%2B-e69e45f-vs-base-mem.svg)
- [📄table](bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6%2B-e69e45f-vs-base.md)
- [📈time plot](bm-20250327-vultr-x86_64-Yhg1s-avoid_list_critsect-3.14.0a6%2B-e69e45f-vs-base.svg)

