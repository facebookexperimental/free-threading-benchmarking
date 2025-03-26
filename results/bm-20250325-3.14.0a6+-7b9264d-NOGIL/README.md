# Results

- fork: mpage/measure_laiv_try_inc
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [7b9264d](https://github.com/mpage/cpython/commit/7b9264d)
- commit date: 2025-03-25T18:10:01-07:00
- commit merge base: [7bb41aef4b7b8f3c3f07c11b801c5b7f8afaac7f](https://github.com/python/cpython/commit/7bb41aef4b7b8f3c3f07c11b801c5b7f8afaac7f)
- ref: measure_laiv_try_inc

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14073299256)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6%2B-7b9264d.json)

### vs. 3.12.6

- Geometric mean: 1.046x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6%2B-7b9264d-vs-3.12.6.md)
- [📈time plot](bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6%2B-7b9264d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.078x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6%2B-7b9264d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6%2B-7b9264d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x slower (HPT: reliability of 91.35%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6%2B-7b9264d-vs-base-mem.svg)
- [📄table](bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6%2B-7b9264d-vs-base.md)
- [📈time plot](bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6%2B-7b9264d-vs-base.svg)

