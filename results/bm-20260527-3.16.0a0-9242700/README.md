# Results

- fork: python/9242700c149c490c56d2
- version: 3.16.0a0
- config: 
- commit hash: [9242700](https://github.com/python/cpython/commit/9242700)
- commit date: 2026-05-27T18:03:34-04:00
- commit merge base: [24c6bbc92b6dd0ce9b7ff799049498299f70f97d](https://github.com/python/cpython/commit/24c6bbc92b6dd0ce9b7ff799049498299f70f97d)
- ref: 9242700c149c490c56d2

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/26547919115)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260527-vultr-x86_64-python-9242700c149c490c56d2-3.16.0a0-9242700.json)

### vs. 3.12.6

- Geometric mean: 1.067x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260527-vultr-x86_64-python-9242700c149c490c56d2-3.16.0a0-9242700-vs-3.12.6.md)
- [📈time plot](bm-20260527-vultr-x86_64-python-9242700c149c490c56d2-3.16.0a0-9242700-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.028x faster (HPT: reliability of 99.92%, 1.01x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260527-vultr-x86_64-python-9242700c149c490c56d2-3.16.0a0-9242700-vs-3.13.0rc2.md)
- [📈time plot](bm-20260527-vultr-x86_64-python-9242700c149c490c56d2-3.16.0a0-9242700-vs-3.13.0rc2.svg)

