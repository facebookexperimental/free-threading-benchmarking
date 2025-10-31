# Results

- fork: python/ac1ffd77858b62d169a0
- version: 3.15.0a1+
- config: NOGIL
- commit hash: [ac1ffd7](https://github.com/python/cpython/commit/ac1ffd7)
- commit date: 2025-10-30T15:29:39-07:00
- commit merge base: [abd19eddee20a7d05266f11f6042a84b04d29664](https://github.com/python/cpython/commit/abd19eddee20a7d05266f11f6042a84b04d29664)
- ref: ac1ffd77858b62d169a0

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18958887411)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251030-vultr-x86_64-python-ac1ffd77858b62d169a0-3.15.0a1%2B-ac1ffd7.json)

### vs. 3.12.6

- Geometric mean: 1.015x slower (HPT: reliability of 82.39%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251030-vultr-x86_64-python-ac1ffd77858b62d169a0-3.15.0a1%2B-ac1ffd7-vs-3.12.6.md)
- [📈time plot](bm-20251030-vultr-x86_64-python-ac1ffd77858b62d169a0-3.15.0a1%2B-ac1ffd7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.048x slower (HPT: reliability of 96.65%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251030-vultr-x86_64-python-ac1ffd77858b62d169a0-3.15.0a1%2B-ac1ffd7-vs-3.13.0rc2.md)
- [📈time plot](bm-20251030-vultr-x86_64-python-ac1ffd77858b62d169a0-3.15.0a1%2B-ac1ffd7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.088x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20251030-vultr-x86_64-python-ac1ffd77858b62d169a0-3.15.0a1%2B-ac1ffd7-vs-base-mem.svg)
- [📄table](bm-20251030-vultr-x86_64-python-ac1ffd77858b62d169a0-3.15.0a1%2B-ac1ffd7-vs-base.md)
- [📈time plot](bm-20251030-vultr-x86_64-python-ac1ffd77858b62d169a0-3.15.0a1%2B-ac1ffd7-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18958887411)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1%2B-ac1ffd7.json)

### vs. 3.12.6

- Geometric mean: 1.086x faster (HPT: reliability of 97.39%, 1.00x faster at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1%2B-ac1ffd7-vs-3.12.6.md)
- [📈time plot](bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1%2B-ac1ffd7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.008x faster (HPT: reliability of 68.13%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1%2B-ac1ffd7-vs-3.13.0rc2.md)
- [📈time plot](bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1%2B-ac1ffd7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.020x slower (HPT: reliability of 99.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.13x
- [🧠memory plot](bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1%2B-ac1ffd7-vs-base-mem.svg)
- [📄table](bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1%2B-ac1ffd7-vs-base.md)
- [📈time plot](bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1%2B-ac1ffd7-vs-base.svg)

