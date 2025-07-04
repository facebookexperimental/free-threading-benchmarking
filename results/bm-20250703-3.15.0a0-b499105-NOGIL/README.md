# Results

- fork: python/b4991056f4f44acb50ae
- version: 3.15.0a0
- config: NOGIL
- commit hash: [b499105](https://github.com/python/cpython/commit/b499105)
- commit date: 2025-07-03T14:04:01-07:00
- commit merge base: [0243f97cbadec8d985e63b1daec5d1cbc850cae3](https://github.com/python/cpython/commit/0243f97cbadec8d985e63b1daec5d1cbc850cae3)
- ref: b4991056f4f44acb50ae

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16063094042)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250703-vultr-x86_64-python-b4991056f4f44acb50ae-3.15.0a0-b499105.json)

### vs. 3.12.6

- Geometric mean: 1.023x slower (HPT: reliability of 95.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250703-vultr-x86_64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.12.6.md)
- [📈time plot](bm-20250703-vultr-x86_64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x slower (HPT: reliability of 97.28%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250703-vultr-x86_64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.13.0rc2.md)
- [📈time plot](bm-20250703-vultr-x86_64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.092x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250703-vultr-x86_64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-base-mem.svg)
- [📄table](bm-20250703-vultr-x86_64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-base.md)
- [📈time plot](bm-20250703-vultr-x86_64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16063094042)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105.json)

### vs. 3.12.6

- Geometric mean: 1.098x faster (HPT: reliability of 97.73%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.12.6.md)
- [📈time plot](bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.019x faster (HPT: reliability of 76.31%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.13.0rc2.md)
- [📈time plot](bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.009x faster (HPT: reliability of 81.51%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-base-mem.svg)
- [📄table](bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-base.md)
- [📈time plot](bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-base.svg)

