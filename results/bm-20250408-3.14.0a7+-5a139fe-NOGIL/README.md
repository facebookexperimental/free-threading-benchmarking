# Results

- fork: mpage/restore_load_bearing
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [5a139fe](https://github.com/mpage/cpython/commit/5a139fe)
- commit date: 2025-04-08T15:17:35-07:00
- commit merge base: [f5f1ac84b3b9d688b9e7d5943c975904b6b74513](https://github.com/python/cpython/commit/f5f1ac84b3b9d688b9e7d5943c975904b6b74513)
- ref: restore_load_bearing

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14344664765)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7%2B-5a139fe.json)

### vs. 3.12.6

- Geometric mean: 1.008x slower (HPT: reliability of 98.28%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7%2B-5a139fe-vs-3.12.6.md)
- [📈time plot](bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7%2B-5a139fe-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.040x slower (HPT: reliability of 99.42%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7%2B-5a139fe-vs-3.13.0rc2.md)
- [📈time plot](bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7%2B-5a139fe-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.076x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7%2B-5a139fe-vs-base-mem.svg)
- [📄table](bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7%2B-5a139fe-vs-base.md)
- [📈time plot](bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7%2B-5a139fe-vs-base.svg)

