# Results

- fork: DinoV/8e6401e63fb5808ee518
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [8e6401e](https://github.com/DinoV/cpython/commit/8e6401e)
- commit date: 2026-10-22T11:46:49-07:00
- commit merge base: [a13d6dbe0375670941fa5830aa44fc1df4986947](https://github.com/python/cpython/commit/a13d6dbe0375670941fa5830aa44fc1df4986947)
- ref: 8e6401e63fb5808ee518

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39834486653)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261022-vultr-x86_64-DinoV-8e6401e63fb5808ee518-3.16.0a1%2Bdev-8e6401e.json)

### vs. 3.12.6

- Geometric mean: 1.060x slower (HPT: reliability of 93.72%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261022-vultr-x86_64-DinoV-8e6401e63fb5808ee518-3.16.0a1%2Bdev-8e6401e-vs-3.12.6.md)
- [📈time plot](bm-20261022-vultr-x86_64-DinoV-8e6401e63fb5808ee518-3.16.0a1%2Bdev-8e6401e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.092x slower (HPT: reliability of 99.76%, 1.01x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261022-vultr-x86_64-DinoV-8e6401e63fb5808ee518-3.16.0a1%2Bdev-8e6401e-vs-3.13.0rc2.md)
- [📈time plot](bm-20261022-vultr-x86_64-DinoV-8e6401e63fb5808ee518-3.16.0a1%2Bdev-8e6401e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.025x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20261022-vultr-x86_64-DinoV-8e6401e63fb5808ee518-3.16.0a1%2Bdev-8e6401e-vs-base-mem.svg)
- [📄table](bm-20261022-vultr-x86_64-DinoV-8e6401e63fb5808ee518-3.16.0a1%2Bdev-8e6401e-vs-base.md)
- [📈time plot](bm-20261022-vultr-x86_64-DinoV-8e6401e63fb5808ee518-3.16.0a1%2Bdev-8e6401e-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.131x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.18x
- [📄table](bm-20261022-vultr-x86_64-DinoV-8e6401e63fb5808ee518-3.16.0a1%2Bdev-8e6401e-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20261022-vultr-x86_64-DinoV-8e6401e63fb5808ee518-3.16.0a1%2Bdev-8e6401e-vs-default_base_vs_NOGIL.svg)

