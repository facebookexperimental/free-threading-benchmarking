# Results

- fork: colesbury/gh_142472_stackrefs
- version: 3.15.0a2+
- config: NOGIL
- commit hash: [a2c45c6](https://github.com/colesbury/cpython/commit/a2c45c6)
- commit date: 2025-12-09T12:39:04-05:00
- commit merge base: [b20722c300a78c38462081a3f1c45190b5434e71](https://github.com/python/cpython/commit/b20722c300a78c38462081a3f1c45190b5434e71)
- ref: gh_142472_stackrefs

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20072680397)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2%2B-a2c45c6.json)

### vs. 3.12.6

- Geometric mean: 1.027x slower (HPT: reliability of 82.89%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2%2B-a2c45c6-vs-3.12.6.md)
- [📈time plot](bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2%2B-a2c45c6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.060x slower (HPT: reliability of 97.06%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2%2B-a2c45c6-vs-3.13.0rc2.md)
- [📈time plot](bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2%2B-a2c45c6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.013x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2%2B-a2c45c6-vs-base-mem.svg)
- [📄table](bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2%2B-a2c45c6-vs-base.md)
- [📈time plot](bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2%2B-a2c45c6-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.098x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [📄table](bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2%2B-a2c45c6-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2%2B-a2c45c6-vs-default_base_vs_NOGIL.svg)

