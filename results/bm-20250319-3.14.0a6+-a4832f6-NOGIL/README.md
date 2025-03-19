# Results

- fork: python/a4832f6b9a62771725b1
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [a4832f6](https://github.com/python/cpython/commit/a4832f6)
- commit date: 2025-03-19T18:27:55+01:00
- commit merge base: [5c44d7d99c470b4270b2f0e4841cf5a7f2499e15](https://github.com/python/cpython/commit/5c44d7d99c470b4270b2f0e4841cf5a7f2499e15)
- ref: a4832f6b9a62771725b1

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13956179961)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250319-vultr-x86_64-python-a4832f6b9a62771725b1-3.14.0a6%2B-a4832f6.json)

### vs. 3.12.6

- Geometric mean: 1.047x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250319-vultr-x86_64-python-a4832f6b9a62771725b1-3.14.0a6%2B-a4832f6-vs-3.12.6.md)
- [📈time plot](bm-20250319-vultr-x86_64-python-a4832f6b9a62771725b1-3.14.0a6%2B-a4832f6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.079x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250319-vultr-x86_64-python-a4832f6b9a62771725b1-3.14.0a6%2B-a4832f6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250319-vultr-x86_64-python-a4832f6b9a62771725b1-3.14.0a6%2B-a4832f6-vs-3.13.0rc2.svg)

