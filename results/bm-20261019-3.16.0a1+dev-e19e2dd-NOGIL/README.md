# Results

- fork: DinoV/e19e2dd8803d6c355634
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [e19e2dd](https://github.com/DinoV/cpython/commit/e19e2dd)
- commit date: 2026-10-19T16:50:42-07:00
- commit merge base: [415ebffc47e8303d61cf97faf4ddb474334d736d](https://github.com/python/cpython/commit/415ebffc47e8303d61cf97faf4ddb474334d736d)
- ref: e19e2dd8803d6c355634

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39346123598)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261019-vultr-x86_64-DinoV-e19e2dd8803d6c355634-3.16.0a1%2Bdev-e19e2dd.json)

### vs. 3.12.6

- Geometric mean: 1.040x slower (HPT: reliability of 79.51%, 1.00x slower at 99th %ile)
- Memory usage: 1.64x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261019-vultr-x86_64-DinoV-e19e2dd8803d6c355634-3.16.0a1%2Bdev-e19e2dd-vs-3.12.6.md)
- [📈time plot](bm-20261019-vultr-x86_64-DinoV-e19e2dd8803d6c355634-3.16.0a1%2Bdev-e19e2dd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.073x slower (HPT: reliability of 97.29%, 1.00x slower at 99th %ile)
- Memory usage: 1.63x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261019-vultr-x86_64-DinoV-e19e2dd8803d6c355634-3.16.0a1%2Bdev-e19e2dd-vs-3.13.0rc2.md)
- [📈time plot](bm-20261019-vultr-x86_64-DinoV-e19e2dd8803d6c355634-3.16.0a1%2Bdev-e19e2dd-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x slower (HPT: reliability of 93.45%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- [🧠memory plot](bm-20261019-vultr-x86_64-DinoV-e19e2dd8803d6c355634-3.16.0a1%2Bdev-e19e2dd-vs-base-mem.svg)
- [📄table](bm-20261019-vultr-x86_64-DinoV-e19e2dd8803d6c355634-3.16.0a1%2Bdev-e19e2dd-vs-base.md)
- [📈time plot](bm-20261019-vultr-x86_64-DinoV-e19e2dd8803d6c355634-3.16.0a1%2Bdev-e19e2dd-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.112x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.35x
- [📄table](bm-20261019-vultr-x86_64-DinoV-e19e2dd8803d6c355634-3.16.0a1%2Bdev-e19e2dd-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20261019-vultr-x86_64-DinoV-e19e2dd8803d6c355634-3.16.0a1%2Bdev-e19e2dd-vs-default_base_vs_NOGIL.svg)

