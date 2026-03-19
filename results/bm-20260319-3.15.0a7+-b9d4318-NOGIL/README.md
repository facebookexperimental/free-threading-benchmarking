# Results

- fork: python/b9d43188e93967c3695e
- version: 3.15.0a7+
- config: NOGIL
- commit hash: [b9d4318](https://github.com/python/cpython/commit/b9d4318)
- commit date: 2026-03-19T00:28:21+01:00
- commit merge base: [656abe3c9a228d20b2455f216a5a94b1a752495f](https://github.com/python/cpython/commit/656abe3c9a228d20b2455f216a5a94b1a752495f)
- ref: b9d43188e93967c3695e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23274112814)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260319-vultr-x86_64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318.json)

### vs. 3.12.6

- Geometric mean: 1.017x slower (HPT: reliability of 54.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260319-vultr-x86_64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.12.6.md)
- [📈time plot](bm-20260319-vultr-x86_64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.050x slower (HPT: reliability of 80.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260319-vultr-x86_64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.13.0rc2.md)
- [📈time plot](bm-20260319-vultr-x86_64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.084x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20260319-vultr-x86_64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-base-mem.svg)
- [📄table](bm-20260319-vultr-x86_64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-base.md)
- [📈time plot](bm-20260319-vultr-x86_64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23274112814)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260319-macm4pro-arm64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318.json)

### vs. 3.12.6

- Geometric mean: 1.105x faster (HPT: reliability of 99.96%, 1.01x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260319-macm4pro-arm64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.12.6.md)
- [📈time plot](bm-20260319-macm4pro-arm64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.025x faster (HPT: reliability of 61.25%, 1.00x faster at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260319-macm4pro-arm64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.13.0rc2.md)
- [📈time plot](bm-20260319-macm4pro-arm64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.047x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260319-macm4pro-arm64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-base-mem.svg)
- [📄table](bm-20260319-macm4pro-arm64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-base.md)
- [📈time plot](bm-20260319-macm4pro-arm64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-base.svg)

