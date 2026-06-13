# Results

- fork: python/80f9467434cecbc4e97b
- version: 3.16.0a0
- config: 
- commit hash: [80f9467](https://github.com/python/cpython/commit/80f9467)
- commit date: 2026-06-11T18:11:52-04:00
- commit merge base: [71805db4294de9495954571c82a835d94ba67594](https://github.com/python/cpython/commit/71805db4294de9495954571c82a835d94ba67594)
- ref: 80f9467434cecbc4e97b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/27387864843)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260611-vultr-x86_64-python-80f9467434cecbc4e97b-3.16.0a0-80f9467.json)

### vs. 3.12.6

- Geometric mean: 1.067x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260611-vultr-x86_64-python-80f9467434cecbc4e97b-3.16.0a0-80f9467-vs-3.12.6.md)
- [📈time plot](bm-20260611-vultr-x86_64-python-80f9467434cecbc4e97b-3.16.0a0-80f9467-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.028x faster (HPT: reliability of 99.78%, 1.00x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260611-vultr-x86_64-python-80f9467434cecbc4e97b-3.16.0a0-80f9467-vs-3.13.0rc2.md)
- [📈time plot](bm-20260611-vultr-x86_64-python-80f9467434cecbc4e97b-3.16.0a0-80f9467-vs-3.13.0rc2.svg)

