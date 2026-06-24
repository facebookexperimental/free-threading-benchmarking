# Results

- fork: python/5e0747db2f5a063657a1
- version: 3.16.0a0
- config: 
- commit hash: [5e0747d](https://github.com/python/cpython/commit/5e0747d)
- commit date: 2026-06-23T16:31:47-04:00
- commit merge base: [10d1b63ed8b0261e7a9b7ffc3231eafd89187a4b](https://github.com/python/cpython/commit/10d1b63ed8b0261e7a9b7ffc3231eafd89187a4b)
- ref: 5e0747db2f5a063657a1

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/28067641645)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260623-vultr-x86_64-python-5e0747db2f5a063657a1-3.16.0a0-5e0747d.json)

### vs. 3.12.6

- Geometric mean: 1.076x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260623-vultr-x86_64-python-5e0747db2f5a063657a1-3.16.0a0-5e0747d-vs-3.12.6.md)
- [📈time plot](bm-20260623-vultr-x86_64-python-5e0747db2f5a063657a1-3.16.0a0-5e0747d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.039x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260623-vultr-x86_64-python-5e0747db2f5a063657a1-3.16.0a0-5e0747d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260623-vultr-x86_64-python-5e0747db2f5a063657a1-3.16.0a0-5e0747d-vs-3.13.0rc2.svg)

