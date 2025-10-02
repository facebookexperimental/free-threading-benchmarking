# Results

- fork: python/75b1afe562c02962393c
- version: 3.15.0a0
- config: NOGIL
- commit hash: [75b1afe](https://github.com/python/cpython/commit/75b1afe)
- commit date: 2025-10-01T21:18:54+01:00
- commit merge base: [76b07c035c224fdfd7bafe5dbc087d0e88469c62](https://github.com/python/cpython/commit/76b07c035c224fdfd7bafe5dbc087d0e88469c62)
- ref: 75b1afe562c02962393c

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18179511805)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251001-vultr-x86_64-python-75b1afe562c02962393c-3.15.0a0-75b1afe.json)

### vs. 3.12.6

- Geometric mean: 1.018x slower (HPT: reliability of 83.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251001-vultr-x86_64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.12.6.md)
- [📈time plot](bm-20251001-vultr-x86_64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.051x slower (HPT: reliability of 96.40%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251001-vultr-x86_64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.13.0rc2.md)
- [📈time plot](bm-20251001-vultr-x86_64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.089x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20251001-vultr-x86_64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-base-mem.svg)
- [📄table](bm-20251001-vultr-x86_64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-base.md)
- [📈time plot](bm-20251001-vultr-x86_64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18179511805)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251001-macm4pro-arm64-python-75b1afe562c02962393c-3.15.0a0-75b1afe.json)

### vs. 3.12.6

- Geometric mean: 1.085x faster (HPT: reliability of 95.15%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251001-macm4pro-arm64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.12.6.md)
- [📈time plot](bm-20251001-macm4pro-arm64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.007x faster (HPT: reliability of 67.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251001-macm4pro-arm64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.13.0rc2.md)
- [📈time plot](bm-20251001-macm4pro-arm64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.000x faster (HPT: reliability of 91.60%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20251001-macm4pro-arm64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-base-mem.svg)
- [📄table](bm-20251001-macm4pro-arm64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-base.md)
- [📈time plot](bm-20251001-macm4pro-arm64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-base.svg)

