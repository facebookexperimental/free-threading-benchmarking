# Results

- fork: python/75ce53d3e2f10347080a
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [75ce53d](https://github.com/python/cpython/commit/75ce53d)
- commit date: 2026-10-16T21:19:02+01:00
- commit merge base: [9cb7a5ba22a51d92a2e321e84ec0287d931f6a9b](https://github.com/python/cpython/commit/9cb7a5ba22a51d92a2e321e84ec0287d931f6a9b)
- ref: 75ce53d3e2f10347080a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39323250040)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261016-vultr-x86_64-python-75ce53d3e2f10347080a-3.16.0a1%2Bdev-75ce53d.json)

### vs. 3.12.6

- Geometric mean: 1.036x slower (HPT: reliability of 81.83%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261016-vultr-x86_64-python-75ce53d3e2f10347080a-3.16.0a1%2Bdev-75ce53d-vs-3.12.6.md)
- [📈time plot](bm-20261016-vultr-x86_64-python-75ce53d3e2f10347080a-3.16.0a1%2Bdev-75ce53d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.069x slower (HPT: reliability of 94.08%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261016-vultr-x86_64-python-75ce53d3e2f10347080a-3.16.0a1%2Bdev-75ce53d-vs-3.13.0rc2.md)
- [📈time plot](bm-20261016-vultr-x86_64-python-75ce53d3e2f10347080a-3.16.0a1%2Bdev-75ce53d-vs-3.13.0rc2.svg)

