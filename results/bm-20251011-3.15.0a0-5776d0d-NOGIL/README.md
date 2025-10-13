# Results

- fork: python/5776d0d2e08f4d93dcd6
- version: 3.15.0a0
- config: NOGIL
- commit hash: [5776d0d](https://github.com/python/cpython/commit/5776d0d)
- commit date: 2025-10-11T15:14:29+00:00
- commit merge base: [2eb32add92d553b320850975442fa2e55addc377](https://github.com/python/cpython/commit/2eb32add92d553b320850975442fa2e55addc377)
- ref: 5776d0d2e08f4d93dcd6

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18473503438)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251011-vultr-x86_64-python-5776d0d2e08f4d93dcd6-3.15.0a0-5776d0d.json)

### vs. 3.12.6

- Geometric mean: 1.017x slower (HPT: reliability of 80.60%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251011-vultr-x86_64-python-5776d0d2e08f4d93dcd6-3.15.0a0-5776d0d-vs-3.12.6.md)
- [📈time plot](bm-20251011-vultr-x86_64-python-5776d0d2e08f4d93dcd6-3.15.0a0-5776d0d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.050x slower (HPT: reliability of 93.76%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251011-vultr-x86_64-python-5776d0d2e08f4d93dcd6-3.15.0a0-5776d0d-vs-3.13.0rc2.md)
- [📈time plot](bm-20251011-vultr-x86_64-python-5776d0d2e08f4d93dcd6-3.15.0a0-5776d0d-vs-3.13.0rc2.svg)

