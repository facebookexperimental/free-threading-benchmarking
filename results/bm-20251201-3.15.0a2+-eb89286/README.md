# Results

- fork: python/eb892868b31322d7cf27
- version: 3.15.0a2+
- config: 
- commit hash: [eb89286](https://github.com/python/cpython/commit/eb89286)
- commit date: 2025-12-01T19:04:47-05:00
- commit merge base: [e32c9756408a3b88394f687c4f55789a8bd21b73](https://github.com/python/cpython/commit/e32c9756408a3b88394f687c4f55789a8bd21b73)
- ref: eb892868b31322d7cf27

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19842288468)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251201-vultr-x86_64-python-eb892868b31322d7cf27-3.15.0a2%2B-eb89286.json)

### vs. 3.12.6

- Geometric mean: 1.080x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251201-vultr-x86_64-python-eb892868b31322d7cf27-3.15.0a2%2B-eb89286-vs-3.12.6.md)
- [📈time plot](bm-20251201-vultr-x86_64-python-eb892868b31322d7cf27-3.15.0a2%2B-eb89286-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.044x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251201-vultr-x86_64-python-eb892868b31322d7cf27-3.15.0a2%2B-eb89286-vs-3.13.0rc2.md)
- [📈time plot](bm-20251201-vultr-x86_64-python-eb892868b31322d7cf27-3.15.0a2%2B-eb89286-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x slower (HPT: reliability of 67.26%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20251201-vultr-x86_64-python-eb892868b31322d7cf27-3.15.0a2%2B-eb89286-vs-base-mem.svg)
- [📄table](bm-20251201-vultr-x86_64-python-eb892868b31322d7cf27-3.15.0a2%2B-eb89286-vs-base.md)
- [📈time plot](bm-20251201-vultr-x86_64-python-eb892868b31322d7cf27-3.15.0a2%2B-eb89286-vs-base.svg)

