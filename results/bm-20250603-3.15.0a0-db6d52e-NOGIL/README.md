# Results

- fork: nascheme/gh_132380_tp_lookup_
- version: 3.15.0a0
- config: NOGIL
- commit hash: [db6d52e](https://github.com/nascheme/cpython/commit/db6d52e)
- commit date: 2025-06-03T12:37:23-07:00
- commit merge base: [1ffe913c2017b44804aca18befd45689df06c069](https://github.com/python/cpython/commit/1ffe913c2017b44804aca18befd45689df06c069)
- ref: gh_132380_tp_lookup_

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15430733994)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e.json)

### vs. 3.12.6

- Geometric mean: 1.015x faster (HPT: reliability of 84.54%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e-vs-3.12.6.md)
- [📈time plot](bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.020x slower (HPT: reliability of 96.65%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x slower (HPT: reliability of 62.39%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e-vs-base-mem.svg)
- [📄table](bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e-vs-base.md)
- [📈time plot](bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.088x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.22x
- [📄table](bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e-vs-default_base_vs_NOGIL.svg)

