# Results

- fork: python/ae7fc4a4f6b711173bb7
- version: 3.15.0a6+
- config: NOGIL
- commit hash: [ae7fc4a](https://github.com/python/cpython/commit/ae7fc4a)
- commit date: 2026-02-23T18:51:03-05:00
- commit merge base: [0e4b1ba55dee1da7bc19d370e784483cd64b12e7](https://github.com/python/cpython/commit/0e4b1ba55dee1da7bc19d370e784483cd64b12e7)
- ref: ae7fc4a4f6b711173bb7

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22331254928)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260223-vultr-x86_64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a.json)

### vs. 3.12.6

- Geometric mean: 1.033x slower (HPT: reliability of 72.72%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260223-vultr-x86_64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.12.6.md)
- [📈time plot](bm-20260223-vultr-x86_64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.065x slower (HPT: reliability of 91.79%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260223-vultr-x86_64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.13.0rc2.md)
- [📈time plot](bm-20260223-vultr-x86_64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.105x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260223-vultr-x86_64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-base-mem.svg)
- [📄table](bm-20260223-vultr-x86_64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-base.md)
- [📈time plot](bm-20260223-vultr-x86_64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22331254928)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a.json)

### vs. 3.12.6

- Geometric mean: 1.088x faster (HPT: reliability of 98.72%, 1.00x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.12.6.md)
- [📈time plot](bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.009x faster (HPT: reliability of 67.87%, 1.00x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.13.0rc2.md)
- [📈time plot](bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.059x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-base-mem.svg)
- [📄table](bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-base.md)
- [📈time plot](bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-base.svg)

