# Results

- fork: python/3c38feb2a21aacdb009e
- version: 3.15.0a7+
- config: NOGIL
- commit hash: [3c38feb](https://github.com/python/cpython/commit/3c38feb)
- commit date: 2026-03-13T19:44:51+01:00
- commit merge base: [747ef70faa8637ccf6dd896323fa84aee8f14513](https://github.com/python/cpython/commit/747ef70faa8637ccf6dd896323fa84aee8f14513)
- ref: 3c38feb2a21aacdb009e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23076207640)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb.json)

### vs. 3.12.6

- Geometric mean: 1.022x slower (HPT: reliability of 71.27%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.12.6.md)
- [📈time plot](bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x slower (HPT: reliability of 88.84%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.13.0rc2.md)
- [📈time plot](bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.093x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-base-mem.svg)
- [📄table](bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-base.md)
- [📈time plot](bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23076207640)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260313-macm4pro-arm64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb.json)

### vs. 3.12.6

- Geometric mean: 1.101x faster (HPT: reliability of 99.93%, 1.01x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260313-macm4pro-arm64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.12.6.md)
- [📈time plot](bm-20260313-macm4pro-arm64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.022x faster (HPT: reliability of 51.63%, 1.00x faster at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260313-macm4pro-arm64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.13.0rc2.md)
- [📈time plot](bm-20260313-macm4pro-arm64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.057x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260313-macm4pro-arm64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-base-mem.svg)
- [📄table](bm-20260313-macm4pro-arm64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-base.md)
- [📈time plot](bm-20260313-macm4pro-arm64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-base.svg)

