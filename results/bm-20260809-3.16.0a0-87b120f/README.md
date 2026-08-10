# Results

- fork: python/87b120fdb58afd8f7cb7
- version: 3.16.0a0
- config: 
- commit hash: [87b120f](https://github.com/python/cpython/commit/87b120f)
- commit date: 2026-08-09T21:06:42+00:00
- commit merge base: [1286d4398e505f70f97e50edda6b0341f16ca267](https://github.com/python/cpython/commit/1286d4398e505f70f97e50edda6b0341f16ca267)
- ref: 87b120fdb58afd8f7cb7

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/31344424487)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f.json)

### vs. 3.12.6

- Geometric mean: 1.072x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f-vs-3.12.6.md)
- [📈time plot](bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.036x faster (HPT: reliability of 99.94%, 1.01x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f-vs-3.13.0rc2.md)
- [📈time plot](bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f-vs-3.13.0rc2.svg)

