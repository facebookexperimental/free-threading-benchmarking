# Results

- fork: python/ed73c909f278a1eb558b
- version: 3.15.0a1+
- config: NOGIL
- commit hash: [ed73c90](https://github.com/python/cpython/commit/ed73c90)
- commit date: 2025-11-15T20:19:41Z
- commit merge base: [85f3009d7504ddcc01de715c494067e89c16303c](https://github.com/python/cpython/commit/85f3009d7504ddcc01de715c494067e89c16303c)
- commit date: 2025-11-15T20:19:41+00:00
- ref: ed73c909f278a1eb558b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19397569375)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251115-vultr-x86_64-python-ed73c909f278a1eb558b-3.15.0a1%2B-ed73c90.json)

### vs. 3.12.6

- Geometric mean: 1.017x slower (HPT: reliability of 80.86%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251115-vultr-x86_64-python-ed73c909f278a1eb558b-3.15.0a1%2B-ed73c90-vs-3.12.6.md)
- [📈time plot](bm-20251115-vultr-x86_64-python-ed73c909f278a1eb558b-3.15.0a1%2B-ed73c90-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.050x slower (HPT: reliability of 94.90%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251115-vultr-x86_64-python-ed73c909f278a1eb558b-3.15.0a1%2B-ed73c90-vs-3.13.0rc2.md)
- [📈time plot](bm-20251115-vultr-x86_64-python-ed73c909f278a1eb558b-3.15.0a1%2B-ed73c90-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.087x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20251115-vultr-x86_64-python-ed73c909f278a1eb558b-3.15.0a1%2B-ed73c90-vs-base-mem.svg)
- [📄table](bm-20251115-vultr-x86_64-python-ed73c909f278a1eb558b-3.15.0a1%2B-ed73c90-vs-base.md)
- [📈time plot](bm-20251115-vultr-x86_64-python-ed73c909f278a1eb558b-3.15.0a1%2B-ed73c90-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19397569375)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1%2B-ed73c90.json)

### vs. 3.12.6

- Geometric mean: 1.103x faster (HPT: reliability of 99.87%, 1.01x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1%2B-ed73c90-vs-3.12.6.md)
- [📈time plot](bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1%2B-ed73c90-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.017x faster (HPT: reliability of 50.47%, 1.00x faster at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1%2B-ed73c90-vs-3.13.0rc2.md)
- [📈time plot](bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1%2B-ed73c90-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.037x slower (HPT: reliability of 99.98%, 1.01x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1%2B-ed73c90-vs-base-mem.svg)
- [📄table](bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1%2B-ed73c90-vs-base.md)
- [📈time plot](bm-20251115-macm4pro-arm64-python-ed73c909f278a1eb558b-3.15.0a1%2B-ed73c90-vs-base.svg)

