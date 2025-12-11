# Results

- fork: colesbury/gh_142472_stackrefs
- version: 3.15.0a2+
- config: 
- commit hash: [7cfe81b](https://github.com/colesbury/cpython/commit/7cfe81b)
- commit date: 2025-12-11T17:50:15+00:00
- commit merge base: [387f88cac1e911672f6321f4fbb0a3af9710626d](https://github.com/python/cpython/commit/387f88cac1e911672f6321f4fbb0a3af9710626d)
- ref: gh_142472_stackrefs

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20142410483)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2%2B-7cfe81b.json)

### vs. 3.12.6

- Geometric mean: 1.074x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2%2B-7cfe81b-vs-3.12.6.md)
- [📈time plot](bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2%2B-7cfe81b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.039x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2%2B-7cfe81b-vs-3.13.0rc2.md)
- [📈time plot](bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2%2B-7cfe81b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x slower (HPT: reliability of 96.18%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2%2B-7cfe81b-vs-base-mem.svg)
- [📄table](bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2%2B-7cfe81b-vs-base.md)
- [📈time plot](bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2%2B-7cfe81b-vs-base.svg)

