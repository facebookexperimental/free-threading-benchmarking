# Results

- fork: python/5d2edf72d25c2616f0e1
- version: 3.15.0a1+
- config: NOGIL
- commit hash: [5d2edf7](https://github.com/python/cpython/commit/5d2edf7)
- commit date: 2025-10-23T22:35:17+02:00
- commit merge base: [f0291c3f2df8139870359c7d1d9a4858f19ee7bf](https://github.com/python/cpython/commit/f0291c3f2df8139870359c7d1d9a4858f19ee7bf)
- ref: 5d2edf72d25c2616f0e1

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18765723543)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251023-vultr-x86_64-python-5d2edf72d25c2616f0e1-3.15.0a1%2B-5d2edf7.json)

### vs. 3.12.6

- Geometric mean: 1.018x slower (HPT: reliability of 86.50%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251023-vultr-x86_64-python-5d2edf72d25c2616f0e1-3.15.0a1%2B-5d2edf7-vs-3.12.6.md)
- [📈time plot](bm-20251023-vultr-x86_64-python-5d2edf72d25c2616f0e1-3.15.0a1%2B-5d2edf7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.051x slower (HPT: reliability of 97.75%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251023-vultr-x86_64-python-5d2edf72d25c2616f0e1-3.15.0a1%2B-5d2edf7-vs-3.13.0rc2.md)
- [📈time plot](bm-20251023-vultr-x86_64-python-5d2edf72d25c2616f0e1-3.15.0a1%2B-5d2edf7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.090x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20251023-vultr-x86_64-python-5d2edf72d25c2616f0e1-3.15.0a1%2B-5d2edf7-vs-base-mem.svg)
- [📄table](bm-20251023-vultr-x86_64-python-5d2edf72d25c2616f0e1-3.15.0a1%2B-5d2edf7-vs-base.md)
- [📈time plot](bm-20251023-vultr-x86_64-python-5d2edf72d25c2616f0e1-3.15.0a1%2B-5d2edf7-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18765723543)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1%2B-5d2edf7.json)

### vs. 3.12.6

- Geometric mean: 1.086x faster (HPT: reliability of 97.48%, 1.00x faster at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1%2B-5d2edf7-vs-3.12.6.md)
- [📈time plot](bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1%2B-5d2edf7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.008x faster (HPT: reliability of 63.08%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1%2B-5d2edf7-vs-3.13.0rc2.md)
- [📈time plot](bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1%2B-5d2edf7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.011x slower (HPT: reliability of 97.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.13x
- [🧠memory plot](bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1%2B-5d2edf7-vs-base-mem.svg)
- [📄table](bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1%2B-5d2edf7-vs-base.md)
- [📈time plot](bm-20251023-macm4pro-arm64-python-5d2edf72d25c2616f0e1-3.15.0a1%2B-5d2edf7-vs-base.svg)

