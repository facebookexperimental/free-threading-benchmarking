# Results

- fork: python/235fa7244a0474c492ae
- version: 3.15.0a8+
- config: JIT
- commit hash: [235fa72](https://github.com/python/cpython/commit/235fa72)
- commit date: 2026-04-12T00:14:50Z
- commit merge base: [d761f539bdae6090817438ae65c0be8a10c9e4e3](https://github.com/python/cpython/commit/d761f539bdae6090817438ae65c0be8a10c9e4e3)
- commit date: 2026-04-12T00:14:50+00:00
- ref: 235fa7244a0474c492ae

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24294885504)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260412-vultr-x86_64-python-235fa7244a0474c492ae-3.15.0a8%2B-235fa72.json)

### vs. 3.12.6

- Geometric mean: 1.171x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, asyncio_tcp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260412-vultr-x86_64-python-235fa7244a0474c492ae-3.15.0a8%2B-235fa72-vs-3.12.6.md)
- [📈time plot](bm-20260412-vultr-x86_64-python-235fa7244a0474c492ae-3.15.0a8%2B-235fa72-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.131x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, asyncio_tcp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260412-vultr-x86_64-python-235fa7244a0474c492ae-3.15.0a8%2B-235fa72-vs-3.13.0rc2.md)
- [📈time plot](bm-20260412-vultr-x86_64-python-235fa7244a0474c492ae-3.15.0a8%2B-235fa72-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.090x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: 🔴 asyncio_tcp
- [🧠memory plot](bm-20260412-vultr-x86_64-python-235fa7244a0474c492ae-3.15.0a8%2B-235fa72-vs-base-mem.svg)
- [📄table](bm-20260412-vultr-x86_64-python-235fa7244a0474c492ae-3.15.0a8%2B-235fa72-vs-base.md)
- [📈time plot](bm-20260412-vultr-x86_64-python-235fa7244a0474c492ae-3.15.0a8%2B-235fa72-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24294885504)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260412-macm4pro-arm64-python-235fa7244a0474c492ae-3.15.0a8%2B-235fa72.json)

### vs. 3.12.6

- Geometric mean: 1.273x faster (HPT: reliability of 100.00%, 1.12x faster at 99th %ile)
- Memory usage: 1.28x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260412-macm4pro-arm64-python-235fa7244a0474c492ae-3.15.0a8%2B-235fa72-vs-3.12.6.md)
- [📈time plot](bm-20260412-macm4pro-arm64-python-235fa7244a0474c492ae-3.15.0a8%2B-235fa72-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.181x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260412-macm4pro-arm64-python-235fa7244a0474c492ae-3.15.0a8%2B-235fa72-vs-3.13.0rc2.md)
- [📈time plot](bm-20260412-macm4pro-arm64-python-235fa7244a0474c492ae-3.15.0a8%2B-235fa72-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.097x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20260412-macm4pro-arm64-python-235fa7244a0474c492ae-3.15.0a8%2B-235fa72-vs-base-mem.svg)
- [📄table](bm-20260412-macm4pro-arm64-python-235fa7244a0474c492ae-3.15.0a8%2B-235fa72-vs-base.md)
- [📈time plot](bm-20260412-macm4pro-arm64-python-235fa7244a0474c492ae-3.15.0a8%2B-235fa72-vs-base.svg)

