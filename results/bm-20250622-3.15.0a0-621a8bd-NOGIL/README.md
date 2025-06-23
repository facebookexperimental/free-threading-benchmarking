# Results

- fork: python/621a8bd6a8d97cf4c628
- version: 3.15.0a0
- config: NOGIL
- commit hash: [621a8bd](https://github.com/python/cpython/commit/621a8bd)
- commit date: 2025-06-22T20:04:38Z
- commit merge base: [b57b619e34cdfc87b47943c988b0b4d69f8f1fe4](https://github.com/python/cpython/commit/b57b619e34cdfc87b47943c988b0b4d69f8f1fe4)
- commit date: 2025-06-22T20:04:38+00:00
- ref: 621a8bd6a8d97cf4c628

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15812467798)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250622-vultr-x86_64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd.json)

### vs. 3.12.6

- Geometric mean: 1.015x faster (HPT: reliability of 82.76%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250622-vultr-x86_64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd-vs-3.12.6.md)
- [📈time plot](bm-20250622-vultr-x86_64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.020x slower (HPT: reliability of 95.83%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250622-vultr-x86_64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd-vs-3.13.0rc2.md)
- [📈time plot](bm-20250622-vultr-x86_64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.085x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250622-vultr-x86_64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd-vs-base-mem.svg)
- [📄table](bm-20250622-vultr-x86_64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd-vs-base.md)
- [📈time plot](bm-20250622-vultr-x86_64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15812467798)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd.json)

### vs. 3.12.6

- Geometric mean: 1.093x faster (HPT: reliability of 97.32%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd-vs-3.12.6.md)
- [📈time plot](bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.014x faster (HPT: reliability of 74.08%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd-vs-3.13.0rc2.md)
- [📈time plot](bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.009x slower (HPT: reliability of 96.28%, 1.00x slower at 99th %ile)
- Memory usage: 1.13x
- [🧠memory plot](bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd-vs-base-mem.svg)
- [📄table](bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd-vs-base.md)
- [📈time plot](bm-20250622-macm4pro-arm64-python-621a8bd6a8d97cf4c628-3.15.0a0-621a8bd-vs-base.svg)

