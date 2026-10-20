# Results

- fork: python/415ebffc47e8303d61cf
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [415ebff](https://github.com/python/cpython/commit/415ebff)
- commit date: 2026-10-19T12:48:08-04:00
- commit merge base: [036d309cf542986a39eeba5ca805b2ec7619731d](https://github.com/python/cpython/commit/036d309cf542986a39eeba5ca805b2ec7619731d)
- ref: 415ebffc47e8303d61cf

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39346123598)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261019-vultr-x86_64-python-415ebffc47e8303d61cf-3.16.0a1%2Bdev-415ebff.json)

### vs. 3.12.6

- Geometric mean: 1.036x slower (HPT: reliability of 70.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261019-vultr-x86_64-python-415ebffc47e8303d61cf-3.16.0a1%2Bdev-415ebff-vs-3.12.6.md)
- [📈time plot](bm-20261019-vultr-x86_64-python-415ebffc47e8303d61cf-3.16.0a1%2Bdev-415ebff-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.069x slower (HPT: reliability of 94.31%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261019-vultr-x86_64-python-415ebffc47e8303d61cf-3.16.0a1%2Bdev-415ebff-vs-3.13.0rc2.md)
- [📈time plot](bm-20261019-vultr-x86_64-python-415ebffc47e8303d61cf-3.16.0a1%2Bdev-415ebff-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.109x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20261019-vultr-x86_64-python-415ebffc47e8303d61cf-3.16.0a1%2Bdev-415ebff-vs-base-mem.svg)
- [📄table](bm-20261019-vultr-x86_64-python-415ebffc47e8303d61cf-3.16.0a1%2Bdev-415ebff-vs-base.md)
- [📈time plot](bm-20261019-vultr-x86_64-python-415ebffc47e8303d61cf-3.16.0a1%2Bdev-415ebff-vs-base.svg)

