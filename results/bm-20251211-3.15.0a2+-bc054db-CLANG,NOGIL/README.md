# Results

- fork: colesbury/gh_120321_gen_atomic
- version: 3.15.0a2+
- config: CLANG,NOGIL
- commit hash: [bc054db](https://github.com/colesbury/cpython/commit/bc054db)
- commit date: 2025-12-11T15:46:51-05:00
- commit merge base: [dac4589726952be873df13f41bea24cc6f9da6b1](https://github.com/python/cpython/commit/dac4589726952be873df13f41bea24cc6f9da6b1)
- ref: gh_120321_gen_atomic

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20149215310)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2%2B-bc054db.json)

### vs. 3.12.6

- Geometric mean: 1.025x faster (HPT: reliability of 95.96%, 1.00x faster at 99th %ile)
- Memory usage: 1.45x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2%2B-bc054db-vs-3.12.6.md)
- [📈time plot](bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2%2B-bc054db-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.009x slower (HPT: reliability of 57.79%, 1.00x faster at 99th %ile)
- Memory usage: 1.44x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2%2B-bc054db-vs-3.13.0rc2.md)
- [📈time plot](bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2%2B-bc054db-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x slower (HPT: reliability of 91.08%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2%2B-bc054db-vs-base-mem.svg)
- [📄table](bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2%2B-bc054db-vs-base.md)
- [📈time plot](bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2%2B-bc054db-vs-base.svg)

