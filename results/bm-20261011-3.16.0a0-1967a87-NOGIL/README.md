# Results

- fork: python/1967a87ad395552dbd1e
- version: 3.16.0a0
- config: NOGIL
- commit hash: [1967a87](https://github.com/python/cpython/commit/1967a87)
- commit date: 2026-10-11T15:53:04-07:00
- commit merge base: [b3714a5fb7a3aadd72134ee0710b22519c1df09a](https://github.com/python/cpython/commit/b3714a5fb7a3aadd72134ee0710b22519c1df09a)
- ref: 1967a87ad395552dbd1e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/38273442374)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261011-vultr-x86_64-python-1967a87ad395552dbd1e-3.16.0a0-1967a87.json)

### vs. 3.12.6

- Geometric mean: 1.040x slower (HPT: reliability of 80.49%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261011-vultr-x86_64-python-1967a87ad395552dbd1e-3.16.0a0-1967a87-vs-3.12.6.md)
- [📈time plot](bm-20261011-vultr-x86_64-python-1967a87ad395552dbd1e-3.16.0a0-1967a87-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.073x slower (HPT: reliability of 93.66%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261011-vultr-x86_64-python-1967a87ad395552dbd1e-3.16.0a0-1967a87-vs-3.13.0rc2.md)
- [📈time plot](bm-20261011-vultr-x86_64-python-1967a87ad395552dbd1e-3.16.0a0-1967a87-vs-3.13.0rc2.svg)

