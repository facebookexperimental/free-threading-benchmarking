# Results

- fork: python/16d0c89b875c520cf5af
- version: 3.16.0a0
- config: 
- commit hash: [16d0c89](https://github.com/python/cpython/commit/16d0c89)
- commit date: 2026-07-18T01:43:38+02:00
- commit merge base: [d478cf81f770168e3fb512ce110a88774f04f549](https://github.com/python/cpython/commit/d478cf81f770168e3fb512ce110a88774f04f549)
- ref: 16d0c89b875c520cf5af

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/29623565103)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260718-vultr-x86_64-python-16d0c89b875c520cf5af-3.16.0a0-16d0c89.json)

### vs. 3.12.6

- Geometric mean: 1.075x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260718-vultr-x86_64-python-16d0c89b875c520cf5af-3.16.0a0-16d0c89-vs-3.12.6.md)
- [📈time plot](bm-20260718-vultr-x86_64-python-16d0c89b875c520cf5af-3.16.0a0-16d0c89-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.040x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260718-vultr-x86_64-python-16d0c89b875c520cf5af-3.16.0a0-16d0c89-vs-3.13.0rc2.md)
- [📈time plot](bm-20260718-vultr-x86_64-python-16d0c89b875c520cf5af-3.16.0a0-16d0c89-vs-3.13.0rc2.svg)

