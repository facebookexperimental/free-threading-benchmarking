# Results

- fork: python/b3bf2128989e550a7a02
- version: 3.15.0a2+
- config: NOGIL
- commit hash: [b3bf212](https://github.com/python/cpython/commit/b3bf212)
- commit date: 2025-12-04T20:28:08+00:00
- commit merge base: [2dac9e6016c81abbefa4256253ff5c59b29378a7](https://github.com/python/cpython/commit/2dac9e6016c81abbefa4256253ff5c59b29378a7)
- ref: b3bf2128989e550a7a02

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19948487271)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251204-vultr-x86_64-python-b3bf2128989e550a7a02-3.15.0a2%2B-b3bf212.json)

### vs. 3.12.6

- Geometric mean: 1.035x slower (HPT: reliability of 88.93%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251204-vultr-x86_64-python-b3bf2128989e550a7a02-3.15.0a2%2B-b3bf212-vs-3.12.6.md)
- [📈time plot](bm-20251204-vultr-x86_64-python-b3bf2128989e550a7a02-3.15.0a2%2B-b3bf212-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.067x slower (HPT: reliability of 97.65%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251204-vultr-x86_64-python-b3bf2128989e550a7a02-3.15.0a2%2B-b3bf212-vs-3.13.0rc2.md)
- [📈time plot](bm-20251204-vultr-x86_64-python-b3bf2128989e550a7a02-3.15.0a2%2B-b3bf212-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.109x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20251204-vultr-x86_64-python-b3bf2128989e550a7a02-3.15.0a2%2B-b3bf212-vs-base-mem.svg)
- [📄table](bm-20251204-vultr-x86_64-python-b3bf2128989e550a7a02-3.15.0a2%2B-b3bf212-vs-base.md)
- [📈time plot](bm-20251204-vultr-x86_64-python-b3bf2128989e550a7a02-3.15.0a2%2B-b3bf212-vs-base.svg)

