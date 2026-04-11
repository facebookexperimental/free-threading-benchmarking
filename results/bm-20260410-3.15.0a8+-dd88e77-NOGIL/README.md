# Results

- fork: python/dd88e77fad887aaf00ea
- version: 3.15.0a8+
- config: NOGIL
- commit hash: [dd88e77](https://github.com/python/cpython/commit/dd88e77)
- commit date: 2026-04-10T19:33:24Z
- commit merge base: [c4d95124b1aa8d2ce8661c3fb8da5da731b14656](https://github.com/python/cpython/commit/c4d95124b1aa8d2ce8661c3fb8da5da731b14656)
- commit date: 2026-04-10T19:33:24+00:00
- ref: dd88e77fad887aaf00ea

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24270557873)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77.json)

### vs. 3.12.6

- Geometric mean: 1.027x slower (HPT: reliability of 63.15%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.12.6.md)
- [📈time plot](bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.059x slower (HPT: reliability of 89.64%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.13.0rc2.md)
- [📈time plot](bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.090x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-base-mem.svg)
- [📄table](bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-base.md)
- [📈time plot](bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24270557873)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77.json)

### vs. 3.12.6

- Geometric mean: 1.106x faster (HPT: reliability of 99.93%, 1.01x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.12.6.md)
- [📈time plot](bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.026x faster (HPT: reliability of 68.26%, 1.00x faster at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.13.0rc2.md)
- [📈time plot](bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.063x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-base-mem.svg)
- [📄table](bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-base.md)
- [📈time plot](bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-base.svg)

