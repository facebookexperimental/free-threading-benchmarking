# Results

- fork: python/24828e57e17621fff166
- version: 3.16.0a0
- config: 
- commit hash: [24828e5](https://github.com/python/cpython/commit/24828e5)
- commit date: 2026-06-22T06:49:54+08:00
- commit merge base: [7782794850f1ba7f100ca65daf4caa083a3b5101](https://github.com/python/cpython/commit/7782794850f1ba7f100ca65daf4caa083a3b5101)
- ref: 24828e57e17621fff166

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/27923591776)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260622-vultr-x86_64-python-24828e57e17621fff166-3.16.0a0-24828e5.json)

### vs. 3.12.6

- Geometric mean: 1.076x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260622-vultr-x86_64-python-24828e57e17621fff166-3.16.0a0-24828e5-vs-3.12.6.md)
- [📈time plot](bm-20260622-vultr-x86_64-python-24828e57e17621fff166-3.16.0a0-24828e5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.039x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260622-vultr-x86_64-python-24828e57e17621fff166-3.16.0a0-24828e5-vs-3.13.0rc2.md)
- [📈time plot](bm-20260622-vultr-x86_64-python-24828e57e17621fff166-3.16.0a0-24828e5-vs-3.13.0rc2.svg)

