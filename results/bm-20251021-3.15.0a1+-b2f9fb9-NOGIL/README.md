# Results

- fork: python/b2f9fb9db29296410f76
- version: 3.15.0a1+
- config: NOGIL
- commit hash: [b2f9fb9](https://github.com/python/cpython/commit/b2f9fb9)
- commit date: 2025-10-21T00:54:44+01:00
- commit merge base: [e09837fcbf39d07c0af51aa936e95c50aed4787c](https://github.com/python/cpython/commit/e09837fcbf39d07c0af51aa936e95c50aed4787c)
- ref: b2f9fb9db29296410f76

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18668828028)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251021-vultr-x86_64-python-b2f9fb9db29296410f76-3.15.0a1%2B-b2f9fb9.json)

### vs. 3.12.6

- Geometric mean: 1.018x slower (HPT: reliability of 88.57%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251021-vultr-x86_64-python-b2f9fb9db29296410f76-3.15.0a1%2B-b2f9fb9-vs-3.12.6.md)
- [📈time plot](bm-20251021-vultr-x86_64-python-b2f9fb9db29296410f76-3.15.0a1%2B-b2f9fb9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.051x slower (HPT: reliability of 95.66%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251021-vultr-x86_64-python-b2f9fb9db29296410f76-3.15.0a1%2B-b2f9fb9-vs-3.13.0rc2.md)
- [📈time plot](bm-20251021-vultr-x86_64-python-b2f9fb9db29296410f76-3.15.0a1%2B-b2f9fb9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.086x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20251021-vultr-x86_64-python-b2f9fb9db29296410f76-3.15.0a1%2B-b2f9fb9-vs-base-mem.svg)
- [📄table](bm-20251021-vultr-x86_64-python-b2f9fb9db29296410f76-3.15.0a1%2B-b2f9fb9-vs-base.md)
- [📈time plot](bm-20251021-vultr-x86_64-python-b2f9fb9db29296410f76-3.15.0a1%2B-b2f9fb9-vs-base.svg)

