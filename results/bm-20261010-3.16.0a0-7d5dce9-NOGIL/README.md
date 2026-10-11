# Results

- fork: python/7d5dce9b1f0da209d172
- version: 3.16.0a0
- config: NOGIL
- commit hash: [7d5dce9](https://github.com/python/cpython/commit/7d5dce9)
- commit date: 2026-10-10T10:39:29+02:00
- commit merge base: [0ec3aee262b03276a18aeb23cb9957e1b57c9d08](https://github.com/python/cpython/commit/0ec3aee262b03276a18aeb23cb9957e1b57c9d08)
- ref: 7d5dce9b1f0da209d172

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/38101770166)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261010-vultr-x86_64-python-7d5dce9b1f0da209d172-3.16.0a0-7d5dce9.json)

### vs. 3.12.6

- Geometric mean: 1.041x slower (HPT: reliability of 75.49%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261010-vultr-x86_64-python-7d5dce9b1f0da209d172-3.16.0a0-7d5dce9-vs-3.12.6.md)
- [📈time plot](bm-20261010-vultr-x86_64-python-7d5dce9b1f0da209d172-3.16.0a0-7d5dce9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.074x slower (HPT: reliability of 93.47%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261010-vultr-x86_64-python-7d5dce9b1f0da209d172-3.16.0a0-7d5dce9-vs-3.13.0rc2.md)
- [📈time plot](bm-20261010-vultr-x86_64-python-7d5dce9b1f0da209d172-3.16.0a0-7d5dce9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x faster (HPT: reliability of 67.19%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20261010-vultr-x86_64-python-7d5dce9b1f0da209d172-3.16.0a0-7d5dce9-vs-base-mem.svg)
- [📄table](bm-20261010-vultr-x86_64-python-7d5dce9b1f0da209d172-3.16.0a0-7d5dce9-vs-base.md)
- [📈time plot](bm-20261010-vultr-x86_64-python-7d5dce9b1f0da209d172-3.16.0a0-7d5dce9-vs-base.svg)

