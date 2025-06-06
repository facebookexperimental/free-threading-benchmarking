# Results

- fork: mpage/restore_load_bearing
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [ccaa69a](https://github.com/mpage/cpython/commit/ccaa69a)
- commit date: 2025-04-02T17:06:45-07:00
- commit merge base: [6bd96894269be4754a811fb8ea1e3b627a676562](https://github.com/python/cpython/commit/6bd96894269be4754a811fb8ea1e3b627a676562)
- ref: restore_load_bearing

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14231997048)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6%2B-ccaa69a.json)

### vs. 3.12.6

- Geometric mean: 1.003x slower (HPT: reliability of 97.84%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6%2B-ccaa69a-vs-3.12.6.md)
- [📈time plot](bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6%2B-ccaa69a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.035x slower (HPT: reliability of 97.72%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6%2B-ccaa69a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6%2B-ccaa69a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.077x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6%2B-ccaa69a-vs-base-mem.svg)
- [📄table](bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6%2B-ccaa69a-vs-base.md)
- [📈time plot](bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6%2B-ccaa69a-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.075x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6%2B-ccaa69a-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6%2B-ccaa69a-vs-default_base_vs_NOGIL.svg)

