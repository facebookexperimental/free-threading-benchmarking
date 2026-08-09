# Results

- fork: python/5ffefdb108094a44e843
- version: 3.16.0a0
- config: NOGIL
- commit hash: [5ffefdb](https://github.com/python/cpython/commit/5ffefdb)
- commit date: 2026-08-07T15:16:25-07:00
- commit merge base: [115400b5090f14233b72b255e483b4485c868100](https://github.com/python/cpython/commit/115400b5090f14233b72b255e483b4485c868100)
- ref: 5ffefdb108094a44e843

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/31229936421)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260807-vultr-x86_64-python-5ffefdb108094a44e843-3.16.0a0-5ffefdb.json)

### vs. 3.12.6

- Geometric mean: 1.037x slower (HPT: reliability of 82.99%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260807-vultr-x86_64-python-5ffefdb108094a44e843-3.16.0a0-5ffefdb-vs-3.12.6.md)
- [📈time plot](bm-20260807-vultr-x86_64-python-5ffefdb108094a44e843-3.16.0a0-5ffefdb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.069x slower (HPT: reliability of 99.29%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260807-vultr-x86_64-python-5ffefdb108094a44e843-3.16.0a0-5ffefdb-vs-3.13.0rc2.md)
- [📈time plot](bm-20260807-vultr-x86_64-python-5ffefdb108094a44e843-3.16.0a0-5ffefdb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.103x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20260807-vultr-x86_64-python-5ffefdb108094a44e843-3.16.0a0-5ffefdb-vs-base-mem.svg)
- [📄table](bm-20260807-vultr-x86_64-python-5ffefdb108094a44e843-3.16.0a0-5ffefdb-vs-base.md)
- [📈time plot](bm-20260807-vultr-x86_64-python-5ffefdb108094a44e843-3.16.0a0-5ffefdb-vs-base.svg)

