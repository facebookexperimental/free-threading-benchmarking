# Results

- fork: python/386d9d071cee2168bee1
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [386d9d0](https://github.com/python/cpython/commit/386d9d0)
- commit date: 2026-10-30T05:32:10+09:00
- commit merge base: [2e1666f1f24c128a9a85bd39680c59aee90f2275](https://github.com/python/cpython/commit/2e1666f1f24c128a9a85bd39680c59aee90f2275)
- ref: 386d9d071cee2168bee1

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/41108757564)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261030-vultr-x86_64-python-386d9d071cee2168bee1-3.16.0a1%2Bdev-386d9d0.json)

### vs. 3.12.6

- Geometric mean: 1.033x slower (HPT: reliability of 73.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261030-vultr-x86_64-python-386d9d071cee2168bee1-3.16.0a1%2Bdev-386d9d0-vs-3.12.6.md)
- [📈time plot](bm-20261030-vultr-x86_64-python-386d9d071cee2168bee1-3.16.0a1%2Bdev-386d9d0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.065x slower (HPT: reliability of 91.50%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261030-vultr-x86_64-python-386d9d071cee2168bee1-3.16.0a1%2Bdev-386d9d0-vs-3.13.0rc2.md)
- [📈time plot](bm-20261030-vultr-x86_64-python-386d9d071cee2168bee1-3.16.0a1%2Bdev-386d9d0-vs-3.13.0rc2.svg)

