# Results

- fork: python/1a0edb1fa899c067f19b
- version: 3.15.0a8+
- config: NOGIL
- commit hash: [1a0edb1](https://github.com/python/cpython/commit/1a0edb1)
- commit date: 2026-04-09T16:21:49-04:00
- commit merge base: [0f492326647a760ab6d66d20334c3308df64a02d](https://github.com/python/cpython/commit/0f492326647a760ab6d66d20334c3308df64a02d)
- ref: 1a0edb1fa899c067f19b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24220558669)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260409-vultr-x86_64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1.json)

### vs. 3.12.6

- Geometric mean: 1.026x slower (HPT: reliability of 62.24%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260409-vultr-x86_64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.12.6.md)
- [📈time plot](bm-20260409-vultr-x86_64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.059x slower (HPT: reliability of 94.38%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260409-vultr-x86_64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.13.0rc2.md)
- [📈time plot](bm-20260409-vultr-x86_64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.092x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260409-vultr-x86_64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-base-mem.svg)
- [📄table](bm-20260409-vultr-x86_64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-base.md)
- [📈time plot](bm-20260409-vultr-x86_64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24220558669)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1.json)

### vs. 3.12.6

- Geometric mean: 1.102x faster (HPT: reliability of 99.91%, 1.01x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.12.6.md)
- [📈time plot](bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.022x faster (HPT: reliability of 63.22%, 1.00x faster at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.13.0rc2.md)
- [📈time plot](bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.055x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-base-mem.svg)
- [📄table](bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-base.md)
- [📈time plot](bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-base.svg)

