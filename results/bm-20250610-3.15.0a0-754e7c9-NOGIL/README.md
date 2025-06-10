# Results

- fork: python/754e7c9b5187fcad22ac
- version: 3.15.0a0
- config: NOGIL
- commit hash: [754e7c9](https://github.com/python/cpython/commit/754e7c9)
- commit date: 2025-06-10T01:08:30+01:00
- commit merge base: [49fc1f215aeb0f71445505191ccb65517b58a5aa](https://github.com/python/cpython/commit/49fc1f215aeb0f71445505191ccb65517b58a5aa)
- ref: 754e7c9b5187fcad22ac

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15547651615)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250610-vultr-x86_64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9.json)

### vs. 3.12.6

- Geometric mean: 1.011x faster (HPT: reliability of 90.80%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250610-vultr-x86_64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9-vs-3.12.6.md)
- [📈time plot](bm-20250610-vultr-x86_64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.024x slower (HPT: reliability of 96.58%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250610-vultr-x86_64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250610-vultr-x86_64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.087x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250610-vultr-x86_64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9-vs-base-mem.svg)
- [📄table](bm-20250610-vultr-x86_64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9-vs-base.md)
- [📈time plot](bm-20250610-vultr-x86_64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15547651615)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9.json)

### vs. 3.12.6

- Geometric mean: 1.095x faster (HPT: reliability of 98.14%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9-vs-3.12.6.md)
- [📈time plot](bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.016x faster (HPT: reliability of 67.66%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.021x slower (HPT: reliability of 98.18%, 1.00x slower at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9-vs-base-mem.svg)
- [📄table](bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9-vs-base.md)
- [📈time plot](bm-20250610-macm4pro-arm64-python-754e7c9b5187fcad22ac-3.15.0a0-754e7c9-vs-base.svg)

