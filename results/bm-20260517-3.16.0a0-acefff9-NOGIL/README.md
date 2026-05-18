# Results

- fork: python/acefff95eab3db6b7cf8
- version: 3.16.0a0
- config: NOGIL
- commit hash: [acefff9](https://github.com/python/cpython/commit/acefff9)
- commit date: 2026-05-17T13:09:19+03:00
- commit merge base: [e62a61177f8b793d787e337034a740ca75c1ab44](https://github.com/python/cpython/commit/e62a61177f8b793d787e337034a740ca75c1ab44)
- ref: acefff95eab3db6b7cf8

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/26007968078)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9.json)

### vs. 3.12.6

- Geometric mean: 1.040x slower (HPT: reliability of 93.91%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9-vs-3.12.6.md)
- [📈time plot](bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.074x slower (HPT: reliability of 99.75%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9-vs-3.13.0rc2.md)
- [📈time plot](bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.099x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9-vs-base-mem.svg)
- [📄table](bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9-vs-base.md)
- [📈time plot](bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/26007968078)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9.json)

### vs. 3.12.6

- Geometric mean: 1.105x faster (HPT: reliability of 99.82%, 1.01x faster at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9-vs-3.12.6.md)
- [📈time plot](bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.021x faster (HPT: reliability of 51.68%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9-vs-3.13.0rc2.md)
- [📈time plot](bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.028x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9-vs-base-mem.svg)
- [📄table](bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9-vs-base.md)
- [📈time plot](bm-20260517-macm4pro-arm64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9-vs-base.svg)

