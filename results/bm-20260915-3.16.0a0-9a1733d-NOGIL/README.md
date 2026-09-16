# Results

- fork: python/9a1733d5712545db0703
- version: 3.16.0a0
- config: NOGIL
- commit hash: [9a1733d](https://github.com/python/cpython/commit/9a1733d)
- commit date: 2026-09-15T23:18:12+02:00
- commit merge base: [e2ca4dc94c553c34578d229c8254b55464045641](https://github.com/python/cpython/commit/e2ca4dc94c553c34578d229c8254b55464045641)
- ref: 9a1733d5712545db0703

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/35041001658)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260915-vultr-x86_64-python-9a1733d5712545db0703-3.16.0a0-9a1733d.json)

### vs. 3.12.6

- Geometric mean: 1.047x slower (HPT: reliability of 91.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260915-vultr-x86_64-python-9a1733d5712545db0703-3.16.0a0-9a1733d-vs-3.12.6.md)
- [📈time plot](bm-20260915-vultr-x86_64-python-9a1733d5712545db0703-3.16.0a0-9a1733d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.078x slower (HPT: reliability of 99.22%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260915-vultr-x86_64-python-9a1733d5712545db0703-3.16.0a0-9a1733d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260915-vultr-x86_64-python-9a1733d5712545db0703-3.16.0a0-9a1733d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.108x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260915-vultr-x86_64-python-9a1733d5712545db0703-3.16.0a0-9a1733d-vs-base-mem.svg)
- [📄table](bm-20260915-vultr-x86_64-python-9a1733d5712545db0703-3.16.0a0-9a1733d-vs-base.md)
- [📈time plot](bm-20260915-vultr-x86_64-python-9a1733d5712545db0703-3.16.0a0-9a1733d-vs-base.svg)

