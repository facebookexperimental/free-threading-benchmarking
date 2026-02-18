# Results

- fork: python/e779777c66595acc5991
- version: 3.15.0a6+
- config: NOGIL
- commit hash: [e779777](https://github.com/python/cpython/commit/e779777)
- commit date: 2026-02-17T23:03:22+01:00
- commit merge base: [d1b541b047e15bb6bddea50a64d71ddb01935e33](https://github.com/python/cpython/commit/d1b541b047e15bb6bddea50a64d71ddb01935e33)
- ref: e779777c66595acc5991

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22121619850)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260217-vultr-x86_64-python-e779777c66595acc5991-3.15.0a6%2B-e779777.json)

### vs. 3.12.6

- Geometric mean: 1.036x slower (HPT: reliability of 85.54%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260217-vultr-x86_64-python-e779777c66595acc5991-3.15.0a6%2B-e779777-vs-3.12.6.md)
- [📈time plot](bm-20260217-vultr-x86_64-python-e779777c66595acc5991-3.15.0a6%2B-e779777-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.068x slower (HPT: reliability of 96.83%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260217-vultr-x86_64-python-e779777c66595acc5991-3.15.0a6%2B-e779777-vs-3.13.0rc2.md)
- [📈time plot](bm-20260217-vultr-x86_64-python-e779777c66595acc5991-3.15.0a6%2B-e779777-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.104x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260217-vultr-x86_64-python-e779777c66595acc5991-3.15.0a6%2B-e779777-vs-base-mem.svg)
- [📄table](bm-20260217-vultr-x86_64-python-e779777c66595acc5991-3.15.0a6%2B-e779777-vs-base.md)
- [📈time plot](bm-20260217-vultr-x86_64-python-e779777c66595acc5991-3.15.0a6%2B-e779777-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22121619850)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260217-macm4pro-arm64-python-e779777c66595acc5991-3.15.0a6%2B-e779777.json)

### vs. 3.12.6

- Geometric mean: 1.085x faster (HPT: reliability of 98.76%, 1.00x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260217-macm4pro-arm64-python-e779777c66595acc5991-3.15.0a6%2B-e779777-vs-3.12.6.md)
- [📈time plot](bm-20260217-macm4pro-arm64-python-e779777c66595acc5991-3.15.0a6%2B-e779777-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.007x faster (HPT: reliability of 64.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260217-macm4pro-arm64-python-e779777c66595acc5991-3.15.0a6%2B-e779777-vs-3.13.0rc2.md)
- [📈time plot](bm-20260217-macm4pro-arm64-python-e779777c66595acc5991-3.15.0a6%2B-e779777-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.064x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20260217-macm4pro-arm64-python-e779777c66595acc5991-3.15.0a6%2B-e779777-vs-base-mem.svg)
- [📄table](bm-20260217-macm4pro-arm64-python-e779777c66595acc5991-3.15.0a6%2B-e779777-vs-base.md)
- [📈time plot](bm-20260217-macm4pro-arm64-python-e779777c66595acc5991-3.15.0a6%2B-e779777-vs-base.svg)

