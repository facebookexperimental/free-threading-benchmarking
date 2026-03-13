# Results

- fork: python/08a018ebe0d673e9c352
- version: 3.15.0a7+
- config: 
- commit hash: [08a018e](https://github.com/python/cpython/commit/08a018e)
- commit date: 2026-03-12T23:48:51+01:00
- commit merge base: [f105265538823126dda5bc113fdb72cb2d5d2dbc](https://github.com/python/cpython/commit/f105265538823126dda5bc113fdb72cb2d5d2dbc)
- ref: 08a018ebe0d673e9c352

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23030688089)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260312-vultr-x86_64-python-08a018ebe0d673e9c352-3.15.0a7%2B-08a018e.json)

### vs. 3.12.6

- Geometric mean: 1.071x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260312-vultr-x86_64-python-08a018ebe0d673e9c352-3.15.0a7%2B-08a018e-vs-3.12.6.md)
- [📈time plot](bm-20260312-vultr-x86_64-python-08a018ebe0d673e9c352-3.15.0a7%2B-08a018e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.035x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260312-vultr-x86_64-python-08a018ebe0d673e9c352-3.15.0a7%2B-08a018e-vs-3.13.0rc2.md)
- [📈time plot](bm-20260312-vultr-x86_64-python-08a018ebe0d673e9c352-3.15.0a7%2B-08a018e-vs-3.13.0rc2.svg)

