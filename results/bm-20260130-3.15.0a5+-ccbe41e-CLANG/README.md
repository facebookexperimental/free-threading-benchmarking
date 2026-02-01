# Results

- fork: python/ccbe41e27cdb44103318
- version: 3.15.0a5+
- config: CLANG
- commit hash: [ccbe41e](https://github.com/python/cpython/commit/ccbe41e)
- commit date: 2026-01-30T20:37:52-08:00
- commit merge base: [96e4cd698a3000382f1796366e9c963902381382](https://github.com/python/cpython/commit/96e4cd698a3000382f1796366e9c963902381382)
- ref: ccbe41e27cdb44103318

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21553336132)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260130-vultr-x86_64-python-ccbe41e27cdb44103318-3.15.0a5%2B-ccbe41e.json)

### vs. 3.12.6

- Geometric mean: 1.125x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260130-vultr-x86_64-python-ccbe41e27cdb44103318-3.15.0a5%2B-ccbe41e-vs-3.12.6.md)
- [📈time plot](bm-20260130-vultr-x86_64-python-ccbe41e27cdb44103318-3.15.0a5%2B-ccbe41e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.088x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260130-vultr-x86_64-python-ccbe41e27cdb44103318-3.15.0a5%2B-ccbe41e-vs-3.13.0rc2.md)
- [📈time plot](bm-20260130-vultr-x86_64-python-ccbe41e27cdb44103318-3.15.0a5%2B-ccbe41e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.049x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20260130-vultr-x86_64-python-ccbe41e27cdb44103318-3.15.0a5%2B-ccbe41e-vs-base-mem.svg)
- [📄table](bm-20260130-vultr-x86_64-python-ccbe41e27cdb44103318-3.15.0a5%2B-ccbe41e-vs-base.md)
- [📈time plot](bm-20260130-vultr-x86_64-python-ccbe41e27cdb44103318-3.15.0a5%2B-ccbe41e-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21553336132)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5%2B-ccbe41e.json)

### vs. 3.12.6

- Geometric mean: 1.202x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5%2B-ccbe41e-vs-3.12.6.md)
- [📈time plot](bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5%2B-ccbe41e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.115x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5%2B-ccbe41e-vs-3.13.0rc2.md)
- [📈time plot](bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5%2B-ccbe41e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.020x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 0.98x
- [🧠memory plot](bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5%2B-ccbe41e-vs-base-mem.svg)
- [📄table](bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5%2B-ccbe41e-vs-base.md)
- [📈time plot](bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5%2B-ccbe41e-vs-base.svg)

