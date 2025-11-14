# Results

- fork: python/a486d452c78a7dfcd425
- version: 3.15.0a1+
- config: NOGIL
- commit hash: [a486d45](https://github.com/python/cpython/commit/a486d45)
- commit date: 2025-11-13T21:05:28+02:00
- commit merge base: [209eaff68c3b241c01aece14182cb9ced51526fc](https://github.com/python/cpython/commit/209eaff68c3b241c01aece14182cb9ced51526fc)
- ref: a486d452c78a7dfcd425

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19350201892)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251113-vultr-x86_64-python-a486d452c78a7dfcd425-3.15.0a1%2B-a486d45.json)

### vs. 3.12.6

- Geometric mean: 1.022x slower (HPT: reliability of 94.10%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251113-vultr-x86_64-python-a486d452c78a7dfcd425-3.15.0a1%2B-a486d45-vs-3.12.6.md)
- [📈time plot](bm-20251113-vultr-x86_64-python-a486d452c78a7dfcd425-3.15.0a1%2B-a486d45-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x slower (HPT: reliability of 96.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251113-vultr-x86_64-python-a486d452c78a7dfcd425-3.15.0a1%2B-a486d45-vs-3.13.0rc2.md)
- [📈time plot](bm-20251113-vultr-x86_64-python-a486d452c78a7dfcd425-3.15.0a1%2B-a486d45-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.093x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20251113-vultr-x86_64-python-a486d452c78a7dfcd425-3.15.0a1%2B-a486d45-vs-base-mem.svg)
- [📄table](bm-20251113-vultr-x86_64-python-a486d452c78a7dfcd425-3.15.0a1%2B-a486d45-vs-base.md)
- [📈time plot](bm-20251113-vultr-x86_64-python-a486d452c78a7dfcd425-3.15.0a1%2B-a486d45-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19350201892)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1%2B-a486d45.json)

### vs. 3.12.6

- Geometric mean: 1.100x faster (HPT: reliability of 99.80%, 1.01x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1%2B-a486d45-vs-3.12.6.md)
- [📈time plot](bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1%2B-a486d45-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.014x faster (HPT: reliability of 51.86%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1%2B-a486d45-vs-3.13.0rc2.md)
- [📈time plot](bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1%2B-a486d45-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.036x slower (HPT: reliability of 99.99%, 1.01x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1%2B-a486d45-vs-base-mem.svg)
- [📄table](bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1%2B-a486d45-vs-base.md)
- [📈time plot](bm-20251113-macm4pro-arm64-python-a486d452c78a7dfcd425-3.15.0a1%2B-a486d45-vs-base.svg)

