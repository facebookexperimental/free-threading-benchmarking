# Results

- fork: python/b8e925b4f8f6c5e28fbe
- version: 3.15.0a5+
- config: NOGIL
- commit hash: [b8e925b](https://github.com/python/cpython/commit/b8e925b)
- commit date: 2026-01-14T23:29:17+02:00
- commit merge base: [f4de18498071f2999432e6459e54797159b6646c](https://github.com/python/cpython/commit/f4de18498071f2999432e6459e54797159b6646c)
- ref: b8e925b4f8f6c5e28fbe

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21014993103)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5%2B-b8e925b.json)

### vs. 3.12.6

- Geometric mean: 1.029x slower (HPT: reliability of 74.29%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5%2B-b8e925b-vs-3.12.6.md)
- [📈time plot](bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5%2B-b8e925b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.062x slower (HPT: reliability of 88.10%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5%2B-b8e925b-vs-3.13.0rc2.md)
- [📈time plot](bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5%2B-b8e925b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.102x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5%2B-b8e925b-vs-base-mem.svg)
- [📄table](bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5%2B-b8e925b-vs-base.md)
- [📈time plot](bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5%2B-b8e925b-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21014993103)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5%2B-b8e925b.json)

### vs. 3.12.6

- Geometric mean: 1.084x faster (HPT: reliability of 98.30%, 1.00x faster at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5%2B-b8e925b-vs-3.12.6.md)
- [📈time plot](bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5%2B-b8e925b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.005x faster (HPT: reliability of 72.49%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5%2B-b8e925b-vs-3.13.0rc2.md)
- [📈time plot](bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5%2B-b8e925b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.063x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5%2B-b8e925b-vs-base-mem.svg)
- [📄table](bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5%2B-b8e925b-vs-base.md)
- [📈time plot](bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5%2B-b8e925b-vs-base.svg)

