# Results

- fork: python/a6bc60da02ea37f33d5a
- version: 3.15.0a3+
- config: 
- commit hash: [a6bc60d](https://github.com/python/cpython/commit/a6bc60d)
- commit date: 2026-01-12T17:55:02-06:00
- commit merge base: [298d5440eb83f2dfd5651bac86d1592ec358d54c](https://github.com/python/cpython/commit/298d5440eb83f2dfd5651bac86d1592ec358d54c)
- ref: a6bc60da02ea37f33d5a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20939929029)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3%2B-a6bc60d.json)

### vs. 3.12.6

- Geometric mean: 1.070x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3%2B-a6bc60d-vs-3.12.6.md)
- [📈time plot](bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3%2B-a6bc60d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.035x faster (HPT: reliability of 99.98%, 1.01x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3%2B-a6bc60d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3%2B-a6bc60d-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20939929029)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260112-macm4pro-arm64-python-a6bc60da02ea37f33d5a-3.15.0a3%2B-a6bc60d.json)

### vs. 3.12.6

- Geometric mean: 1.156x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260112-macm4pro-arm64-python-a6bc60da02ea37f33d5a-3.15.0a3%2B-a6bc60d-vs-3.12.6.md)
- [📈time plot](bm-20260112-macm4pro-arm64-python-a6bc60da02ea37f33d5a-3.15.0a3%2B-a6bc60d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.072x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260112-macm4pro-arm64-python-a6bc60da02ea37f33d5a-3.15.0a3%2B-a6bc60d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260112-macm4pro-arm64-python-a6bc60da02ea37f33d5a-3.15.0a3%2B-a6bc60d-vs-3.13.0rc2.svg)

