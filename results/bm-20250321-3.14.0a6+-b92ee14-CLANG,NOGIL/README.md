# Results

- fork: python/b92ee14b80cc8898f799
- version: 3.14.0a6+
- config: CLANG,NOGIL
- commit hash: [b92ee14](https://github.com/python/cpython/commit/b92ee14)
- commit date: 2025-03-21T11:23:12-07:00
- commit merge base: [0de5e0c5442abddbe17481ef450e4abc992058f5](https://github.com/python/cpython/commit/0de5e0c5442abddbe17481ef450e4abc992058f5)
- ref: b92ee14b80cc8898f799

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14084679447)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250321-vultr-x86_64-python-b92ee14b80cc8898f799-3.14.0a6%2B-b92ee14.json)

### vs. 3.12.6

- Geometric mean: 1.044x faster (HPT: reliability of 57.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250321-vultr-x86_64-python-b92ee14b80cc8898f799-3.14.0a6%2B-b92ee14-vs-3.12.6.md)
- [📈time plot](bm-20250321-vultr-x86_64-python-b92ee14b80cc8898f799-3.14.0a6%2B-b92ee14-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.010x faster (HPT: reliability of 89.29%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250321-vultr-x86_64-python-b92ee14b80cc8898f799-3.14.0a6%2B-b92ee14-vs-3.13.0rc2.md)
- [📈time plot](bm-20250321-vultr-x86_64-python-b92ee14b80cc8898f799-3.14.0a6%2B-b92ee14-vs-3.13.0rc2.svg)

