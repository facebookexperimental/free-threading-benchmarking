# Results

- fork: python/1f9d20bbd4fed601e7ca
- version: 3.16.0a0
- config: NOGIL
- commit hash: [1f9d20b](https://github.com/python/cpython/commit/1f9d20b)
- commit date: 2026-07-20T00:19:32+02:00
- commit merge base: [51de91dbb076985d7c656f6a57919846f2556bb7](https://github.com/python/cpython/commit/51de91dbb076985d7c656f6a57919846f2556bb7)
- ref: 1f9d20bbd4fed601e7ca

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/29709923140)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b.json)

### vs. 3.12.6

- Geometric mean: 1.037x slower (HPT: reliability of 92.95%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b-vs-3.12.6.md)
- [📈time plot](bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.069x slower (HPT: reliability of 97.64%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b-vs-3.13.0rc2.md)
- [📈time plot](bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.109x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b-vs-base-mem.svg)
- [📄table](bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b-vs-base.md)
- [📈time plot](bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b-vs-base.svg)

