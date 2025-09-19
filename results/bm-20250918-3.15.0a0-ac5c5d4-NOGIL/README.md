# Results

- fork: python/ac5c5d42a2e542b3d036
- version: 3.15.0a0
- config: NOGIL
- commit hash: [ac5c5d4](https://github.com/python/cpython/commit/ac5c5d4)
- commit date: 2025-09-18T22:08:49+01:00
- commit merge base: [3eec8977528dbbd22f9c0873930507fd97053843](https://github.com/python/cpython/commit/3eec8977528dbbd22f9c0873930507fd97053843)
- ref: ac5c5d42a2e542b3d036

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17844835027)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250918-vultr-x86_64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4.json)

### vs. 3.12.6

- Geometric mean: 1.028x slower (HPT: reliability of 95.79%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250918-vultr-x86_64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4-vs-3.12.6.md)
- [📈time plot](bm-20250918-vultr-x86_64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.061x slower (HPT: reliability of 98.81%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250918-vultr-x86_64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4-vs-3.13.0rc2.md)
- [📈time plot](bm-20250918-vultr-x86_64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.101x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250918-vultr-x86_64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4-vs-base-mem.svg)
- [📄table](bm-20250918-vultr-x86_64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4-vs-base.md)
- [📈time plot](bm-20250918-vultr-x86_64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17844835027)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4.json)

### vs. 3.12.6

- Geometric mean: 1.091x faster (HPT: reliability of 97.79%, 1.00x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4-vs-3.12.6.md)
- [📈time plot](bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.012x faster (HPT: reliability of 62.24%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4-vs-3.13.0rc2.md)
- [📈time plot](bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.006x slower (HPT: reliability of 96.71%, 1.00x slower at 99th %ile)
- Memory usage: 1.10x
- [🧠memory plot](bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4-vs-base-mem.svg)
- [📄table](bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4-vs-base.md)
- [📈time plot](bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4-vs-base.svg)

