# Results

- fork: DinoV/80f2c4377eccfa53236d
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [80f2c43](https://github.com/DinoV/cpython/commit/80f2c43)
- commit date: 2026-11-03T09:59:34-08:00
- commit merge base: [ce841a9a02b9a28367b52b7b0c9606b5bdeacada](https://github.com/python/cpython/commit/ce841a9a02b9a28367b52b7b0c9606b5bdeacada)
- ref: 80f2c4377eccfa53236d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/41690003577)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261103-vultr-x86_64-DinoV-80f2c4377eccfa53236d-3.16.0a1%2Bdev-80f2c43.json)

### vs. 3.12.6

- Geometric mean: 1.104x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261103-vultr-x86_64-DinoV-80f2c4377eccfa53236d-3.16.0a1%2Bdev-80f2c43-vs-3.12.6.md)
- [📈time plot](bm-20261103-vultr-x86_64-DinoV-80f2c4377eccfa53236d-3.16.0a1%2Bdev-80f2c43-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.133x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261103-vultr-x86_64-DinoV-80f2c4377eccfa53236d-3.16.0a1%2Bdev-80f2c43-vs-3.13.0rc2.md)
- [📈time plot](bm-20261103-vultr-x86_64-DinoV-80f2c4377eccfa53236d-3.16.0a1%2Bdev-80f2c43-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.071x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.06x
- [🧠memory plot](bm-20261103-vultr-x86_64-DinoV-80f2c4377eccfa53236d-3.16.0a1%2Bdev-80f2c43-vs-base-mem.svg)
- [📄table](bm-20261103-vultr-x86_64-DinoV-80f2c4377eccfa53236d-3.16.0a1%2Bdev-80f2c43-vs-base.md)
- [📈time plot](bm-20261103-vultr-x86_64-DinoV-80f2c4377eccfa53236d-3.16.0a1%2Bdev-80f2c43-vs-base.svg)

