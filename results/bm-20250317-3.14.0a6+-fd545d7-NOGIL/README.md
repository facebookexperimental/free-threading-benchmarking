# Results

- fork: python/fd545d735d5f9c048f99
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [fd545d7](https://github.com/python/cpython/commit/fd545d7)
- commit date: 2025-03-17T17:23:50+00:00
- commit merge base: [9881fc5483d6298dc969919dddecf2b72ddf8d43](https://github.com/python/cpython/commit/9881fc5483d6298dc969919dddecf2b72ddf8d43)
- ref: fd545d735d5f9c048f99

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13936202028)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7.json)

### vs. 3.12.6

- Geometric mean: 1.047x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7-vs-3.12.6.md)
- [📈time plot](bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.079x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7-vs-3.13.0rc2.md)
- [📈time plot](bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.103x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: 🔴 sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile
- new benchmarks: html5lib, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [🧠memory plot](bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7-vs-base-mem.svg)
- [📄table](bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7-vs-base.md)
- [📈time plot](bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7-vs-base.svg)

