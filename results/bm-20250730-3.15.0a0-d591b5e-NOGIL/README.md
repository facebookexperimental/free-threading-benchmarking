# Results

- fork: python/d591b5effb8ec8177a95
- version: 3.15.0a0
- config: NOGIL
- commit hash: [d591b5e](https://github.com/python/cpython/commit/d591b5e)
- commit date: 2025-07-30T15:48:18-07:00
- commit merge base: [5f35f9b8fad50670604552062c1df8fbdff835ab](https://github.com/python/cpython/commit/5f35f9b8fad50670604552062c1df8fbdff835ab)
- ref: d591b5effb8ec8177a95

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16636783187)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250730-vultr-x86_64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e.json)

### vs. 3.12.6

- Geometric mean: 1.026x slower (HPT: reliability of 93.52%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250730-vultr-x86_64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.12.6.md)
- [📈time plot](bm-20250730-vultr-x86_64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.059x slower (HPT: reliability of 98.55%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250730-vultr-x86_64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250730-vultr-x86_64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.094x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250730-vultr-x86_64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-base-mem.svg)
- [📄table](bm-20250730-vultr-x86_64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-base.md)
- [📈time plot](bm-20250730-vultr-x86_64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16636783187)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e.json)

### vs. 3.12.6

- Geometric mean: 1.085x faster (HPT: reliability of 96.61%, 1.00x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.12.6.md)
- [📈time plot](bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.007x faster (HPT: reliability of 76.31%, 1.00x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.017x slower (HPT: reliability of 95.41%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-base-mem.svg)
- [📄table](bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-base.md)
- [📈time plot](bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-base.svg)

