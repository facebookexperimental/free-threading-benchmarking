# Results

- fork: nascheme/gh_127266_type_slots
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [ca00e74](https://github.com/nascheme/cpython/commit/ca00e74)
- commit date: 2025-03-26T03:10:26-07:00
- commit merge base: [898e6b395e63ad7f8bbe421adf0af8947d429925](https://github.com/python/cpython/commit/898e6b395e63ad7f8bbe421adf0af8947d429925)
- ref: gh_127266_type_slots

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14078184538)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6%2B-ca00e74.json)

### vs. 3.12.6

- Geometric mean: 1.045x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6%2B-ca00e74-vs-3.12.6.md)
- [📈time plot](bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6%2B-ca00e74-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.076x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6%2B-ca00e74-vs-3.13.0rc2.md)
- [📈time plot](bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6%2B-ca00e74-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6%2B-ca00e74-vs-base-mem.svg)
- [📄table](bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6%2B-ca00e74-vs-base.md)
- [📈time plot](bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6%2B-ca00e74-vs-base.svg)

