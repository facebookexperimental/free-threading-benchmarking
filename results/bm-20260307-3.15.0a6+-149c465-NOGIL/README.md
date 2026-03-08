# Results

- fork: python/149c4657507d17f78dd0
- version: 3.15.0a6+
- config: NOGIL
- commit hash: [149c465](https://github.com/python/cpython/commit/149c465)
- commit date: 2026-03-07T16:53:13+02:00
- commit merge base: [2cf6b2caade94e75f10363df6f432a3e6515be6c](https://github.com/python/cpython/commit/2cf6b2caade94e75f10363df6f432a3e6515be6c)
- ref: 149c4657507d17f78dd0

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22810259279)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6%2B-149c465.json)

### vs. 3.12.6

- Geometric mean: 1.023x slower (HPT: reliability of 61.51%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6%2B-149c465-vs-3.12.6.md)
- [📈time plot](bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6%2B-149c465-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.056x slower (HPT: reliability of 83.84%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6%2B-149c465-vs-3.13.0rc2.md)
- [📈time plot](bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6%2B-149c465-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.095x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6%2B-149c465-vs-base-mem.svg)
- [📄table](bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6%2B-149c465-vs-base.md)
- [📈time plot](bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6%2B-149c465-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22810259279)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6%2B-149c465.json)

### vs. 3.12.6

- Geometric mean: 1.100x faster (HPT: reliability of 99.76%, 1.01x faster at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6%2B-149c465-vs-3.12.6.md)
- [📈time plot](bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6%2B-149c465-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.020x faster (HPT: reliability of 60.39%, 1.00x faster at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6%2B-149c465-vs-3.13.0rc2.md)
- [📈time plot](bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6%2B-149c465-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.040x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.11x
- new benchmarks: asyncio_websockets
- [🧠memory plot](bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6%2B-149c465-vs-base-mem.svg)
- [📄table](bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6%2B-149c465-vs-base.md)
- [📈time plot](bm-20260307-macm4pro-arm64-python-149c4657507d17f78dd0-3.15.0a6%2B-149c465-vs-base.svg)

