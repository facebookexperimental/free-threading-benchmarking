# Results

- fork: python/85ec35d2ab8b764aefd6
- version: 3.15.0a0
- config: 
- commit hash: [85ec35d](https://github.com/python/cpython/commit/85ec35d)
- commit date: 2025-10-08T01:19:50+02:00
- commit merge base: [5a77f02d72e0735877fe4a5d615559d1541bc232](https://github.com/python/cpython/commit/5a77f02d72e0735877fe4a5d615559d1541bc232)
- ref: 85ec35d2ab8b764aefd6

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18329912920)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d.json)

### vs. 3.12.6

- Geometric mean: 1.076x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.12.6.md)
- [📈time plot](bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.040x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.13.0rc2.md)
- [📈time plot](bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18329912920)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d.json)

### vs. 3.12.6

- Geometric mean: 1.104x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.12.6.md)
- [📈time plot](bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.024x faster (HPT: reliability of 91.58%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.13.0rc2.md)
- [📈time plot](bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.13.0rc2.svg)

