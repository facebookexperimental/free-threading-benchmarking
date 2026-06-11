# Results

- fork: python/ce916dc50644bb1de940
- version: 3.16.0a0
- config: 
- commit hash: [ce916dc](https://github.com/python/cpython/commit/ce916dc)
- commit date: 2026-06-09T15:22:13-07:00
- commit merge base: [580499177ca91477b53b4a40afcec7d3370265b0](https://github.com/python/cpython/commit/580499177ca91477b53b4a40afcec7d3370265b0)
- ref: ce916dc50644bb1de940

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/27246176708)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260609-vultr-x86_64-python-ce916dc50644bb1de940-3.16.0a0-ce916dc.json)

### vs. 3.12.6

- Geometric mean: 1.069x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260609-vultr-x86_64-python-ce916dc50644bb1de940-3.16.0a0-ce916dc-vs-3.12.6.md)
- [📈time plot](bm-20260609-vultr-x86_64-python-ce916dc50644bb1de940-3.16.0a0-ce916dc-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.029x faster (HPT: reliability of 99.93%, 1.01x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260609-vultr-x86_64-python-ce916dc50644bb1de940-3.16.0a0-ce916dc-vs-3.13.0rc2.md)
- [📈time plot](bm-20260609-vultr-x86_64-python-ce916dc50644bb1de940-3.16.0a0-ce916dc-vs-3.13.0rc2.svg)

