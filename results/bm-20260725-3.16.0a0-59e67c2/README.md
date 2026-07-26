# Results

- fork: python/59e67c284d3e8dcb708e
- version: 3.16.0a0
- config: 
- commit hash: [59e67c2](https://github.com/python/cpython/commit/59e67c2)
- commit date: 2026-07-25T01:40:32+02:00
- commit merge base: [9560bd8f3533ac16684dfe11283bb834af52f10f](https://github.com/python/cpython/commit/9560bd8f3533ac16684dfe11283bb834af52f10f)
- ref: 59e67c284d3e8dcb708e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/30136968125)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260725-vultr-x86_64-python-59e67c284d3e8dcb708e-3.16.0a0-59e67c2.json)

### vs. 3.12.6

- Geometric mean: 1.069x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260725-vultr-x86_64-python-59e67c284d3e8dcb708e-3.16.0a0-59e67c2-vs-3.12.6.md)
- [📈time plot](bm-20260725-vultr-x86_64-python-59e67c284d3e8dcb708e-3.16.0a0-59e67c2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.034x faster (HPT: reliability of 99.84%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260725-vultr-x86_64-python-59e67c284d3e8dcb708e-3.16.0a0-59e67c2-vs-3.13.0rc2.md)
- [📈time plot](bm-20260725-vultr-x86_64-python-59e67c284d3e8dcb708e-3.16.0a0-59e67c2-vs-3.13.0rc2.svg)

