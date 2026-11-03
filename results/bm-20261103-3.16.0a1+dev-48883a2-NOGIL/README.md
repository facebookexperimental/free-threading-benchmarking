# Results

- fork: DinoV/48883a281d72773b18c1
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [48883a2](https://github.com/DinoV/cpython/commit/48883a2)
- commit date: 2026-11-03T10:22:31-08:00
- commit merge base: [ce841a9a02b9a28367b52b7b0c9606b5bdeacada](https://github.com/python/cpython/commit/ce841a9a02b9a28367b52b7b0c9606b5bdeacada)
- ref: 48883a281d72773b18c1

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/41693317724)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261103-vultr-x86_64-DinoV-48883a281d72773b18c1-3.16.0a1%2Bdev-48883a2.json)

### vs. 3.12.6

- Geometric mean: 1.042x slower (HPT: reliability of 85.28%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261103-vultr-x86_64-DinoV-48883a281d72773b18c1-3.16.0a1%2Bdev-48883a2-vs-3.12.6.md)
- [📈time plot](bm-20261103-vultr-x86_64-DinoV-48883a281d72773b18c1-3.16.0a1%2Bdev-48883a2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.073x slower (HPT: reliability of 96.13%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261103-vultr-x86_64-DinoV-48883a281d72773b18c1-3.16.0a1%2Bdev-48883a2-vs-3.13.0rc2.md)
- [📈time plot](bm-20261103-vultr-x86_64-DinoV-48883a281d72773b18c1-3.16.0a1%2Bdev-48883a2-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.008x slower (HPT: reliability of 99.99%, 1.00x slower at 99th %ile)
- Memory usage: 1.04x
- [🧠memory plot](bm-20261103-vultr-x86_64-DinoV-48883a281d72773b18c1-3.16.0a1%2Bdev-48883a2-vs-base-mem.svg)
- [📄table](bm-20261103-vultr-x86_64-DinoV-48883a281d72773b18c1-3.16.0a1%2Bdev-48883a2-vs-base.md)
- [📈time plot](bm-20261103-vultr-x86_64-DinoV-48883a281d72773b18c1-3.16.0a1%2Bdev-48883a2-vs-base.svg)

