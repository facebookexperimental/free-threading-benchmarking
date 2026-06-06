# Results

- fork: python/e28a2f493044ecfc0f76
- version: 3.16.0a0
- config: NOGIL
- commit hash: [e28a2f4](https://github.com/python/cpython/commit/e28a2f4)
- commit date: 2026-06-04T21:37:18+01:00
- commit merge base: [f906522a4e1f4565ae7a449d3556dc8f70591b20](https://github.com/python/cpython/commit/f906522a4e1f4565ae7a449d3556dc8f70591b20)
- ref: e28a2f493044ecfc0f76

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/26989036327)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260604-vultr-x86_64-python-e28a2f493044ecfc0f76-3.16.0a0-e28a2f4.json)

### vs. 3.12.6

- Geometric mean: 1.033x slower (HPT: reliability of 84.72%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260604-vultr-x86_64-python-e28a2f493044ecfc0f76-3.16.0a0-e28a2f4-vs-3.12.6.md)
- [📈time plot](bm-20260604-vultr-x86_64-python-e28a2f493044ecfc0f76-3.16.0a0-e28a2f4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.069x slower (HPT: reliability of 97.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260604-vultr-x86_64-python-e28a2f493044ecfc0f76-3.16.0a0-e28a2f4-vs-3.13.0rc2.md)
- [📈time plot](bm-20260604-vultr-x86_64-python-e28a2f493044ecfc0f76-3.16.0a0-e28a2f4-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.096x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260604-vultr-x86_64-python-e28a2f493044ecfc0f76-3.16.0a0-e28a2f4-vs-base-mem.svg)
- [📄table](bm-20260604-vultr-x86_64-python-e28a2f493044ecfc0f76-3.16.0a0-e28a2f4-vs-base.md)
- [📈time plot](bm-20260604-vultr-x86_64-python-e28a2f493044ecfc0f76-3.16.0a0-e28a2f4-vs-base.svg)

