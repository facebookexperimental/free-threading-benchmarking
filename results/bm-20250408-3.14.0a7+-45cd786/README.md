# Results

- fork: mpage/gh_129987_no_slp_vec
- version: 3.14.0a7+
- config: 
- commit hash: [45cd786](https://github.com/mpage/cpython/commit/45cd786)
- commit date: 2025-04-08T16:58:14-07:00
- commit merge base: [f5f1ac84b3b9d688b9e7d5943c975904b6b74513](https://github.com/python/cpython/commit/f5f1ac84b3b9d688b9e7d5943c975904b6b74513)
- ref: gh_129987_no_slp_vec

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14345935753)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7%2B-45cd786.json)

### vs. 3.12.6

- Geometric mean: 1.119x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7%2B-45cd786-vs-3.12.6.md)
- [📈time plot](bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7%2B-45cd786-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.079x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7%2B-45cd786-vs-3.13.0rc2.md)
- [📈time plot](bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7%2B-45cd786-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.042x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7%2B-45cd786-vs-base-mem.svg)
- [📄table](bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7%2B-45cd786-vs-base.md)
- [📈time plot](bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7%2B-45cd786-vs-base.svg)

