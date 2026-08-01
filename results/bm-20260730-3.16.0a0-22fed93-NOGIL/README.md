# Results

- fork: python/22fed93a21c36c032d87
- version: 3.16.0a0
- config: NOGIL
- commit hash: [22fed93](https://github.com/python/cpython/commit/22fed93)
- commit date: 2026-07-30T17:39:09-05:00
- commit merge base: [60b9cf84117567c5df63482d9fbf68db3d7ef74e](https://github.com/python/cpython/commit/60b9cf84117567c5df63482d9fbf68db3d7ef74e)
- ref: 22fed93a21c36c032d87

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/30594395999)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260730-vultr-x86_64-python-22fed93a21c36c032d87-3.16.0a0-22fed93.json)

### vs. 3.12.6

- Geometric mean: 1.033x slower (HPT: reliability of 78.22%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260730-vultr-x86_64-python-22fed93a21c36c032d87-3.16.0a0-22fed93-vs-3.12.6.md)
- [📈time plot](bm-20260730-vultr-x86_64-python-22fed93a21c36c032d87-3.16.0a0-22fed93-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.065x slower (HPT: reliability of 96.37%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260730-vultr-x86_64-python-22fed93a21c36c032d87-3.16.0a0-22fed93-vs-3.13.0rc2.md)
- [📈time plot](bm-20260730-vultr-x86_64-python-22fed93a21c36c032d87-3.16.0a0-22fed93-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.099x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20260730-vultr-x86_64-python-22fed93a21c36c032d87-3.16.0a0-22fed93-vs-base-mem.svg)
- [📄table](bm-20260730-vultr-x86_64-python-22fed93a21c36c032d87-3.16.0a0-22fed93-vs-base.md)
- [📈time plot](bm-20260730-vultr-x86_64-python-22fed93a21c36c032d87-3.16.0a0-22fed93-vs-base.svg)

