# Results

- fork: Fidget-Spinner/tos_caching_rebased_
- version: 3.15.0a0
- config: JIT
- commit hash: [992ac08](https://github.com/Fidget%2dSpinner/cpython/commit/992ac08)
- commit date: 2025-06-25T02:48:18+08:00
- commit merge base: [bda121862e7d7f4684d9f0281f7d1f408c0c740c](https://github.com/python/cpython/commit/bda121862e7d7f4684d9f0281f7d1f408c0c740c)
- ref: tos_caching_rebased_

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16031614569)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250625-vultr-x86_64-Fidget%252dSpinner-tos_caching_rebased_-3.15.0a0-992ac08.json)

### vs. 3.12.6

- Geometric mean: 1.116x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250625-vultr-x86_64-Fidget%252dSpinner-tos_caching_rebased_-3.15.0a0-992ac08-vs-3.12.6.md)
- [📈time plot](bm-20250625-vultr-x86_64-Fidget%252dSpinner-tos_caching_rebased_-3.15.0a0-992ac08-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.079x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250625-vultr-x86_64-Fidget%252dSpinner-tos_caching_rebased_-3.15.0a0-992ac08-vs-3.13.0rc2.md)
- [📈time plot](bm-20250625-vultr-x86_64-Fidget%252dSpinner-tos_caching_rebased_-3.15.0a0-992ac08-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x faster (HPT: reliability of 98.72%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250625-vultr-x86_64-Fidget%252dSpinner-tos_caching_rebased_-3.15.0a0-992ac08-vs-base-mem.svg)
- [📄table](bm-20250625-vultr-x86_64-Fidget%252dSpinner-tos_caching_rebased_-3.15.0a0-992ac08-vs-base.md)
- [📈time plot](bm-20250625-vultr-x86_64-Fidget%252dSpinner-tos_caching_rebased_-3.15.0a0-992ac08-vs-base.svg)

