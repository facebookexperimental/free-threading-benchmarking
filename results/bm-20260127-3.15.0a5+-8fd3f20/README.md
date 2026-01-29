# Results

- fork: DinoV/lazy_review_updates2
- version: 3.15.0a5+
- config: 
- commit hash: [8fd3f20](https://github.com/DinoV/cpython/commit/8fd3f20)
- commit date: 2026-01-27T17:16:27-08:00
- commit merge base: [c461aa99e2fabbaf5859c0a8a93e08306ee8115d](https://github.com/python/cpython/commit/c461aa99e2fabbaf5859c0a8a93e08306ee8115d)
- ref: lazy_review_updates2

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21450920950)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5%2B-8fd3f20.json)

### vs. 3.12.6

- Geometric mean: 1.042x slower (HPT: reliability of 97.65%, 1.00x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5%2B-8fd3f20-vs-3.12.6.md)
- [📈time plot](bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5%2B-8fd3f20-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.074x slower (HPT: reliability of 99.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5%2B-8fd3f20-vs-3.13.0rc2.md)
- [📈time plot](bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5%2B-8fd3f20-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.105x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.02x
- [🧠memory plot](bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5%2B-8fd3f20-vs-base-mem.svg)
- [📄table](bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5%2B-8fd3f20-vs-base.md)
- [📈time plot](bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5%2B-8fd3f20-vs-base.svg)

