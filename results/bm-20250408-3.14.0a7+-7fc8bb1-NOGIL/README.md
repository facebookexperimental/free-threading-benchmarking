# Results

- fork: mpage/gh_129987_no_slp_vec
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [7fc8bb1](https://github.com/mpage/cpython/commit/7fc8bb1)
- commit date: 2025-04-08T15:14:55-07:00
- commit merge base: [f5f1ac84b3b9d688b9e7d5943c975904b6b74513](https://github.com/python/cpython/commit/f5f1ac84b3b9d688b9e7d5943c975904b6b74513)
- ref: gh_129987_no_slp_vec

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14344637393)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7%2B-7fc8bb1.json)

### vs. 3.12.6

- Geometric mean: 1.012x slower (HPT: reliability of 98.86%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7%2B-7fc8bb1-vs-3.12.6.md)
- [📈time plot](bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7%2B-7fc8bb1-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.044x slower (HPT: reliability of 99.47%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7%2B-7fc8bb1-vs-3.13.0rc2.md)
- [📈time plot](bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7%2B-7fc8bb1-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.072x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7%2B-7fc8bb1-vs-base-mem.svg)
- [📄table](bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7%2B-7fc8bb1-vs-base.md)
- [📈time plot](bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7%2B-7fc8bb1-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.084x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7%2B-7fc8bb1-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7%2B-7fc8bb1-vs-default_base_vs_NOGIL.svg)

