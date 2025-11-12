# Results

- fork: python/0d7b48a8f5de5c1c6d57
- version: 3.15.0a1+
- config: NOGIL
- commit hash: [0d7b48a](https://github.com/python/cpython/commit/0d7b48a)
- commit date: 2025-11-12T00:03:14Z
- commit merge base: [f5c2a41f9a6b3be95c5be9dbae0a4a3342d356dc](https://github.com/python/cpython/commit/f5c2a41f9a6b3be95c5be9dbae0a4a3342d356dc)
- commit date: 2025-11-12T00:03:14+00:00
- ref: 0d7b48a8f5de5c1c6d57

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19282372439)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251112-vultr-x86_64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a.json)

### vs. 3.12.6

- Geometric mean: 1.017x slower (HPT: reliability of 69.44%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251112-vultr-x86_64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.12.6.md)
- [📈time plot](bm-20251112-vultr-x86_64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.050x slower (HPT: reliability of 94.05%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251112-vultr-x86_64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.13.0rc2.md)
- [📈time plot](bm-20251112-vultr-x86_64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.090x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20251112-vultr-x86_64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-base-mem.svg)
- [📄table](bm-20251112-vultr-x86_64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-base.md)
- [📈time plot](bm-20251112-vultr-x86_64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19282372439)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a.json)

### vs. 3.12.6

- Geometric mean: 1.082x faster (HPT: reliability of 96.97%, 1.00x faster at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.12.6.md)
- [📈time plot](bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.002x slower (HPT: reliability of 76.19%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.13.0rc2.md)
- [📈time plot](bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.029x slower (HPT: reliability of 99.94%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-base-mem.svg)
- [📄table](bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-base.md)
- [📈time plot](bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-base.svg)

