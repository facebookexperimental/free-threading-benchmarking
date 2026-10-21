# Results

- fork: DinoV/7c4bdf4fcb908d36d855
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [7c4bdf4](https://github.com/DinoV/cpython/commit/7c4bdf4)
- commit date: 2026-10-21T11:15:02-07:00
- commit merge base: [a13d6dbe0375670941fa5830aa44fc1df4986947](https://github.com/python/cpython/commit/a13d6dbe0375670941fa5830aa44fc1df4986947)
- ref: 7c4bdf4fcb908d36d855

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39679544197)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261021-vultr-x86_64-DinoV-7c4bdf4fcb908d36d855-3.16.0a1%2Bdev-7c4bdf4.json)

### vs. 3.12.6

- Geometric mean: 1.051x slower (HPT: reliability of 91.19%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261021-vultr-x86_64-DinoV-7c4bdf4fcb908d36d855-3.16.0a1%2Bdev-7c4bdf4-vs-3.12.6.md)
- [📈time plot](bm-20261021-vultr-x86_64-DinoV-7c4bdf4fcb908d36d855-3.16.0a1%2Bdev-7c4bdf4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.083x slower (HPT: reliability of 99.47%, 1.00x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261021-vultr-x86_64-DinoV-7c4bdf4fcb908d36d855-3.16.0a1%2Bdev-7c4bdf4-vs-3.13.0rc2.md)
- [📈time plot](bm-20261021-vultr-x86_64-DinoV-7c4bdf4fcb908d36d855-3.16.0a1%2Bdev-7c4bdf4-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.015x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20261021-vultr-x86_64-DinoV-7c4bdf4fcb908d36d855-3.16.0a1%2Bdev-7c4bdf4-vs-base-mem.svg)
- [📄table](bm-20261021-vultr-x86_64-DinoV-7c4bdf4fcb908d36d855-3.16.0a1%2Bdev-7c4bdf4-vs-base.md)
- [📈time plot](bm-20261021-vultr-x86_64-DinoV-7c4bdf4fcb908d36d855-3.16.0a1%2Bdev-7c4bdf4-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.118x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.18x
- [📄table](bm-20261021-vultr-x86_64-DinoV-7c4bdf4fcb908d36d855-3.16.0a1%2Bdev-7c4bdf4-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20261021-vultr-x86_64-DinoV-7c4bdf4fcb908d36d855-3.16.0a1%2Bdev-7c4bdf4-vs-default_base_vs_NOGIL.svg)

