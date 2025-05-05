# Results

- fork: nascheme/gc_check_rss
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [aabe31d](https://github.com/nascheme/cpython/commit/aabe31d)
- commit date: 2025-05-04T15:36:42-07:00
- commit merge base: [af5799f3056b0eee61fc09587633500a3690e67e](https://github.com/python/cpython/commit/af5799f3056b0eee61fc09587633500a3690e67e)
- ref: gc_check_rss

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14829916893)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7%2B-aabe31d.json)

### vs. 3.12.6

- Geometric mean: 1.007x faster (HPT: reliability of 90.90%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7%2B-aabe31d-vs-3.12.6.md)
- [📈time plot](bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7%2B-aabe31d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.025x slower (HPT: reliability of 98.13%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7%2B-aabe31d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7%2B-aabe31d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.007x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7%2B-aabe31d-vs-base-mem.svg)
- [📄table](bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7%2B-aabe31d-vs-base.md)
- [📈time plot](bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7%2B-aabe31d-vs-base.svg)

