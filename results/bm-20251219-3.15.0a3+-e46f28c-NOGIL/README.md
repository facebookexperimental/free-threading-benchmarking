# Results

- fork: python/e46f28c6afce9c85e4bc
- version: 3.15.0a3+
- config: NOGIL
- commit hash: [e46f28c](https://github.com/python/cpython/commit/e46f28c)
- commit date: 2025-12-19T18:06:47-05:00
- commit merge base: [4ea3c1a04747978361b497798428423cbb6a7146](https://github.com/python/cpython/commit/4ea3c1a04747978361b497798428423cbb6a7146)
- ref: e46f28c6afce9c85e4bc

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20386193128)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3%2B-e46f28c.json)

### vs. 3.12.6

- Geometric mean: 1.031x slower (HPT: reliability of 86.71%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3%2B-e46f28c-vs-3.12.6.md)
- [📈time plot](bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3%2B-e46f28c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.063x slower (HPT: reliability of 98.22%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3%2B-e46f28c-vs-3.13.0rc2.md)
- [📈time plot](bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3%2B-e46f28c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.098x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3%2B-e46f28c-vs-base-mem.svg)
- [📄table](bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3%2B-e46f28c-vs-base.md)
- [📈time plot](bm-20251219-vultr-x86_64-python-e46f28c6afce9c85e4bc-3.15.0a3%2B-e46f28c-vs-base.svg)

