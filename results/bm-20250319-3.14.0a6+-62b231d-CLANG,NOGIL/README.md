# Results

- fork: colesbury/experiment_interp_ti
- version: 3.14.0a6+
- config: CLANG,NOGIL
- commit hash: [62b231d](https://github.com/colesbury/cpython/commit/62b231d)
- commit date: 2025-03-19T13:48:34+00:00
- commit merge base: [f5e4c2955ba5977f468e4a61d429526602d96343](https://github.com/python/cpython/commit/f5e4c2955ba5977f468e4a61d429526602d96343)
- ref: experiment_interp_ti

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13948181749)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6%2B-62b231d.json)

### vs. 3.12.6

- Geometric mean: 1.043x faster (HPT: reliability of 77.23%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6%2B-62b231d-vs-3.12.6.md)
- [📈time plot](bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6%2B-62b231d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.009x faster (HPT: reliability of 88.47%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6%2B-62b231d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6%2B-62b231d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x slower (HPT: reliability of 99.21%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6%2B-62b231d-vs-base-mem.svg)
- [📄table](bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6%2B-62b231d-vs-base.md)
- [📈time plot](bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6%2B-62b231d-vs-base.svg)

