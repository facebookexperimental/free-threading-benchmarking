# Results

- fork: python/494f2e3c92cc1b7774cc
- version: 3.16.0a0
- config: 
- commit hash: [494f2e3](https://github.com/python/cpython/commit/494f2e3)
- commit date: 2026-06-03T01:15:34+01:00
- commit merge base: [29805f00a1b65163230d17584c30e2b955086abb](https://github.com/python/cpython/commit/29805f00a1b65163230d17584c30e2b955086abb)
- ref: 494f2e3c92cc1b7774cc

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/26857698621)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260603-vultr-x86_64-python-494f2e3c92cc1b7774cc-3.16.0a0-494f2e3.json)

### vs. 3.12.6

- Geometric mean: 1.066x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260603-vultr-x86_64-python-494f2e3c92cc1b7774cc-3.16.0a0-494f2e3-vs-3.12.6.md)
- [📈time plot](bm-20260603-vultr-x86_64-python-494f2e3c92cc1b7774cc-3.16.0a0-494f2e3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.027x faster (HPT: reliability of 99.87%, 1.00x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260603-vultr-x86_64-python-494f2e3c92cc1b7774cc-3.16.0a0-494f2e3-vs-3.13.0rc2.md)
- [📈time plot](bm-20260603-vultr-x86_64-python-494f2e3c92cc1b7774cc-3.16.0a0-494f2e3-vs-3.13.0rc2.svg)

