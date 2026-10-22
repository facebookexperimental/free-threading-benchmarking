# Results

- fork: python/f65e2a209562b9a4163d
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [f65e2a2](https://github.com/python/cpython/commit/f65e2a2)
- commit date: 2026-10-22T18:42:46+00:00
- commit merge base: [86758d1950ce2ed2626014b52d26d24c74dee55b](https://github.com/python/cpython/commit/86758d1950ce2ed2626014b52d26d24c74dee55b)
- ref: f65e2a209562b9a4163d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39858885239)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261022-vultr-x86_64-python-f65e2a209562b9a4163d-3.16.0a1%2Bdev-f65e2a2.json)

### vs. 3.12.6

- Geometric mean: 1.031x slower (HPT: reliability of 64.10%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261022-vultr-x86_64-python-f65e2a209562b9a4163d-3.16.0a1%2Bdev-f65e2a2-vs-3.12.6.md)
- [📈time plot](bm-20261022-vultr-x86_64-python-f65e2a209562b9a4163d-3.16.0a1%2Bdev-f65e2a2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.064x slower (HPT: reliability of 89.57%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261022-vultr-x86_64-python-f65e2a209562b9a4163d-3.16.0a1%2Bdev-f65e2a2-vs-3.13.0rc2.md)
- [📈time plot](bm-20261022-vultr-x86_64-python-f65e2a209562b9a4163d-3.16.0a1%2Bdev-f65e2a2-vs-3.13.0rc2.svg)

