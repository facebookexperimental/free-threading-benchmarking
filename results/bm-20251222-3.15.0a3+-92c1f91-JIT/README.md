# Results

- fork: diegorusso/executor_register
- version: 3.15.0a3+
- config: JIT
- commit hash: [92c1f91](https://github.com/diegorusso/cpython/commit/92c1f91)
- commit date: 2025-12-22T14:43:25+00:00
- commit merge base: [ff7f62eb2333ac2a2ce2726ba1763bf2fa1956e2](https://github.com/python/cpython/commit/ff7f62eb2333ac2a2ce2726ba1763bf2fa1956e2)
- ref: executor_register

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20465199030)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3%2B-92c1f91.json)

### vs. 3.12.6

- Geometric mean: 1.118x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3%2B-92c1f91-vs-3.12.6.md)
- [📈time plot](bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3%2B-92c1f91-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.080x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3%2B-92c1f91-vs-3.13.0rc2.md)
- [📈time plot](bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3%2B-92c1f91-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.000x faster (HPT: reliability of 86.53%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3%2B-92c1f91-vs-base-mem.svg)
- [📄table](bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3%2B-92c1f91-vs-base.md)
- [📈time plot](bm-20251222-vultr-x86_64-diegorusso-executor_register-3.15.0a3%2B-92c1f91-vs-base.svg)

