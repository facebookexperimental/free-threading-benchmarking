# Results

- fork: python/4084141073127669a779
- version: 3.16.0a0
- config: 
- commit hash: [4084141](https://github.com/python/cpython/commit/4084141)
- commit date: 2026-06-07T19:25:50+01:00
- commit merge base: [81965c1683d7129a70e3fde22ea8a02b9398e227](https://github.com/python/cpython/commit/81965c1683d7129a70e3fde22ea8a02b9398e227)
- ref: 4084141073127669a779

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/27110470105)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260607-vultr-x86_64-python-4084141073127669a779-3.16.0a0-4084141.json)

### vs. 3.12.6

- Geometric mean: 1.071x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260607-vultr-x86_64-python-4084141073127669a779-3.16.0a0-4084141-vs-3.12.6.md)
- [📈time plot](bm-20260607-vultr-x86_64-python-4084141073127669a779-3.16.0a0-4084141-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.031x faster (HPT: reliability of 99.79%, 1.00x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260607-vultr-x86_64-python-4084141073127669a779-3.16.0a0-4084141-vs-3.13.0rc2.md)
- [📈time plot](bm-20260607-vultr-x86_64-python-4084141073127669a779-3.16.0a0-4084141-vs-3.13.0rc2.svg)

