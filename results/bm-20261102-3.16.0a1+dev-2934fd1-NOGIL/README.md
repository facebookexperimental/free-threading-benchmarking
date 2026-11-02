# Results

- fork: DinoV/2934fd1085679c213716
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [2934fd1](https://github.com/DinoV/cpython/commit/2934fd1)
- commit date: 2026-11-02T13:32:15-08:00
- commit merge base: [386d9d071cee2168bee135bc15897a27377d0999](https://github.com/python/cpython/commit/386d9d071cee2168bee135bc15897a27377d0999)
- ref: 2934fd1085679c213716

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/41529338580)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261102-vultr-x86_64-DinoV-2934fd1085679c213716-3.16.0a1%2Bdev-2934fd1.json)

### vs. 3.12.6

- Geometric mean: 1.056x slower (HPT: reliability of 79.79%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261102-vultr-x86_64-DinoV-2934fd1085679c213716-3.16.0a1%2Bdev-2934fd1-vs-3.12.6.md)
- [📈time plot](bm-20261102-vultr-x86_64-DinoV-2934fd1085679c213716-3.16.0a1%2Bdev-2934fd1-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.087x slower (HPT: reliability of 99.72%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261102-vultr-x86_64-DinoV-2934fd1085679c213716-3.16.0a1%2Bdev-2934fd1-vs-3.13.0rc2.md)
- [📈time plot](bm-20261102-vultr-x86_64-DinoV-2934fd1085679c213716-3.16.0a1%2Bdev-2934fd1-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.023x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20261102-vultr-x86_64-DinoV-2934fd1085679c213716-3.16.0a1%2Bdev-2934fd1-vs-base-mem.svg)
- [📄table](bm-20261102-vultr-x86_64-DinoV-2934fd1085679c213716-3.16.0a1%2Bdev-2934fd1-vs-base.md)
- [📈time plot](bm-20261102-vultr-x86_64-DinoV-2934fd1085679c213716-3.16.0a1%2Bdev-2934fd1-vs-base.svg)

