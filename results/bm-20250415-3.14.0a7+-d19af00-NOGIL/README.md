# Results

- fork: python/d19af00b90d94cd98729
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [d19af00](https://github.com/python/cpython/commit/d19af00)
- commit date: 2025-04-15T18:31:52-04:00
- commit merge base: [4f10b93d1b2f887b42ad59168a9fcbe75bdaaf87](https://github.com/python/cpython/commit/4f10b93d1b2f887b42ad59168a9fcbe75bdaaf87)
- ref: d19af00b90d94cd98729

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14481993442)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250415-vultr-x86_64-python-d19af00b90d94cd98729-3.14.0a7%2B-d19af00.json)

### vs. 3.12.6

- Geometric mean: 1.029x faster (HPT: reliability of 60.31%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250415-vultr-x86_64-python-d19af00b90d94cd98729-3.14.0a7%2B-d19af00-vs-3.12.6.md)
- [📈time plot](bm-20250415-vultr-x86_64-python-d19af00b90d94cd98729-3.14.0a7%2B-d19af00-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.005x slower (HPT: reliability of 91.59%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250415-vultr-x86_64-python-d19af00b90d94cd98729-3.14.0a7%2B-d19af00-vs-3.13.0rc2.md)
- [📈time plot](bm-20250415-vultr-x86_64-python-d19af00b90d94cd98729-3.14.0a7%2B-d19af00-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.076x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250415-vultr-x86_64-python-d19af00b90d94cd98729-3.14.0a7%2B-d19af00-vs-base-mem.svg)
- [📄table](bm-20250415-vultr-x86_64-python-d19af00b90d94cd98729-3.14.0a7%2B-d19af00-vs-base.md)
- [📈time plot](bm-20250415-vultr-x86_64-python-d19af00b90d94cd98729-3.14.0a7%2B-d19af00-vs-base.svg)

