# Results

- fork: DinoV/3c8be4f527078397cb43
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [3c8be4f](https://github.com/DinoV/cpython/commit/3c8be4f)
- commit date: 2026-10-20T11:39:16-07:00
- commit merge base: [415ebffc47e8303d61cf97faf4ddb474334d736d](https://github.com/python/cpython/commit/415ebffc47e8303d61cf97faf4ddb474334d736d)
- ref: 3c8be4f527078397cb43

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39476892845)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261020-vultr-x86_64-DinoV-3c8be4f527078397cb43-3.16.0a1%2Bdev-3c8be4f.json)

### vs. 3.12.6

- Geometric mean: 1.033x slower (HPT: reliability of 67.75%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261020-vultr-x86_64-DinoV-3c8be4f527078397cb43-3.16.0a1%2Bdev-3c8be4f-vs-3.12.6.md)
- [📈time plot](bm-20261020-vultr-x86_64-DinoV-3c8be4f527078397cb43-3.16.0a1%2Bdev-3c8be4f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.066x slower (HPT: reliability of 91.65%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261020-vultr-x86_64-DinoV-3c8be4f527078397cb43-3.16.0a1%2Bdev-3c8be4f-vs-3.13.0rc2.md)
- [📈time plot](bm-20261020-vultr-x86_64-DinoV-3c8be4f527078397cb43-3.16.0a1%2Bdev-3c8be4f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x faster (HPT: reliability of 97.69%, 1.00x faster at 99th %ile)
- Memory usage: 1.04x
- [🧠memory plot](bm-20261020-vultr-x86_64-DinoV-3c8be4f527078397cb43-3.16.0a1%2Bdev-3c8be4f-vs-base-mem.svg)
- [📄table](bm-20261020-vultr-x86_64-DinoV-3c8be4f527078397cb43-3.16.0a1%2Bdev-3c8be4f-vs-base.md)
- [📈time plot](bm-20261020-vultr-x86_64-DinoV-3c8be4f527078397cb43-3.16.0a1%2Bdev-3c8be4f-vs-base.svg)

