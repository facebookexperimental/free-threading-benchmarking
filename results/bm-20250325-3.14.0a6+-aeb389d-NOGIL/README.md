# Results

- fork: DinoV/nolock_loadattr_with
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [aeb389d](https://github.com/DinoV/cpython/commit/aeb389d)
- commit date: 2025-03-25T17:04:00-07:00
- commit merge base: [a26a301f8b09c1825b288fc8649f8174576361f4](https://github.com/python/cpython/commit/a26a301f8b09c1825b288fc8649f8174576361f4)
- ref: nolock_loadattr_with

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14089118132)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6%2B-aeb389d.json)

### vs. 3.12.6

- Geometric mean: 1.045x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6%2B-aeb389d-vs-3.12.6.md)
- [📈time plot](bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6%2B-aeb389d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.076x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6%2B-aeb389d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6%2B-aeb389d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x faster (HPT: reliability of 58.02%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6%2B-aeb389d-vs-base-mem.svg)
- [📄table](bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6%2B-aeb389d-vs-base.md)
- [📈time plot](bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6%2B-aeb389d-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.112x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6%2B-aeb389d-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6%2B-aeb389d-vs-default_base_vs_NOGIL.svg)

