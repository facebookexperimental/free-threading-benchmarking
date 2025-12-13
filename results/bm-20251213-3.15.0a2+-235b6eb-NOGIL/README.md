# Results

- fork: nascheme/set_lockfree_contain
- version: 3.15.0a2+
- config: NOGIL
- commit hash: [235b6eb](https://github.com/nascheme/cpython/commit/235b6eb)
- commit date: 2025-12-13T01:17:43-08:00
- commit merge base: [3e36d375352632be85b9ac3a0eeb075a4e03ef6f](https://github.com/python/cpython/commit/3e36d375352632be85b9ac3a0eeb075a4e03ef6f)
- ref: set_lockfree_contain

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20195696014)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2%2B-235b6eb.json)

### vs. 3.12.6

- Geometric mean: 1.034x slower (HPT: reliability of 88.75%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2%2B-235b6eb-vs-3.12.6.md)
- [📈time plot](bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2%2B-235b6eb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.066x slower (HPT: reliability of 96.04%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2%2B-235b6eb-vs-3.13.0rc2.md)
- [📈time plot](bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2%2B-235b6eb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x faster (HPT: reliability of 99.06%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2%2B-235b6eb-vs-base-mem.svg)
- [📄table](bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2%2B-235b6eb-vs-base.md)
- [📈time plot](bm-20251213-vultr-x86_64-nascheme-set_lockfree_contain-3.15.0a2%2B-235b6eb-vs-base.svg)

