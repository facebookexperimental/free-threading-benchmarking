# Results

- fork: nascheme/gh_133136_qsbr_defer
- version: 3.15.0a0
- config: NOGIL
- commit hash: [3978e35](https://github.com/nascheme/cpython/commit/3978e35)
- commit date: 2025-06-12T23:08:58-07:00
- commit merge base: [1ffe913c2017b44804aca18befd45689df06c069](https://github.com/python/cpython/commit/1ffe913c2017b44804aca18befd45689df06c069)
- ref: gh_133136_qsbr_defer

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15627826920)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35.json)

### vs. 3.12.6

- Geometric mean: 1.015x faster (HPT: reliability of 84.65%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35-vs-3.12.6.md)
- [📈time plot](bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.020x slower (HPT: reliability of 95.05%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35-vs-3.13.0rc2.md)
- [📈time plot](bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.000x slower (HPT: reliability of 56.16%, 1.00x faster at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35-vs-base-mem.svg)
- [📄table](bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35-vs-base.md)
- [📈time plot](bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.088x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.21x
- [📄table](bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35-vs-default_base_vs_NOGIL.svg)

