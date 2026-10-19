# Results

- fork: daanx/750480840e28509fe6dc
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [7504808](https://github.com/daanx/cpython/commit/7504808)
- commit date: 2026-10-16T17:32:10-07:00
- commit merge base: [75ce53d3e2f10347080ab466b936ae070f1c5a94](https://github.com/python/cpython/commit/75ce53d3e2f10347080ab466b936ae070f1c5a94)
- ref: 750480840e28509fe6dc

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39289057174)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261016-vultr-x86_64-daanx-750480840e28509fe6dc-3.16.0a1%2Bdev-7504808.json)

### vs. 3.12.6

- Geometric mean: 1.020x slower (HPT: reliability of 52.09%, 1.00x slower at 99th %ile)
- Memory usage: 2.84x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261016-vultr-x86_64-daanx-750480840e28509fe6dc-3.16.0a1%2Bdev-7504808-vs-3.12.6.md)
- [📈time plot](bm-20261016-vultr-x86_64-daanx-750480840e28509fe6dc-3.16.0a1%2Bdev-7504808-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.053x slower (HPT: reliability of 80.21%, 1.00x slower at 99th %ile)
- Memory usage: 2.83x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261016-vultr-x86_64-daanx-750480840e28509fe6dc-3.16.0a1%2Bdev-7504808-vs-3.13.0rc2.md)
- [📈time plot](bm-20261016-vultr-x86_64-daanx-750480840e28509fe6dc-3.16.0a1%2Bdev-7504808-vs-3.13.0rc2.svg)

