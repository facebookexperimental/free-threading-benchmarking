# Results

- fork: python/62143736b623fd0bcf99
- version: 3.15.0a0
- config: NOGIL
- commit hash: [6214373](https://github.com/python/cpython/commit/6214373)
- commit date: 2025-06-11T17:35:48-06:00
- commit merge base: [b706ff003c536c5bca24dfdd3a8917bffcfa3df1](https://github.com/python/cpython/commit/b706ff003c536c5bca24dfdd3a8917bffcfa3df1)
- ref: 62143736b623fd0bcf99

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15598636887)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250611-vultr-x86_64-python-62143736b623fd0bcf99-3.15.0a0-6214373.json)

### vs. 3.12.6

- Geometric mean: 1.012x faster (HPT: reliability of 89.90%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250611-vultr-x86_64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.12.6.md)
- [📈time plot](bm-20250611-vultr-x86_64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.023x slower (HPT: reliability of 95.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250611-vultr-x86_64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.13.0rc2.md)
- [📈time plot](bm-20250611-vultr-x86_64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.087x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250611-vultr-x86_64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-base-mem.svg)
- [📄table](bm-20250611-vultr-x86_64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-base.md)
- [📈time plot](bm-20250611-vultr-x86_64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15598636887)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250611-macm4pro-arm64-python-62143736b623fd0bcf99-3.15.0a0-6214373.json)

### vs. 3.12.6

- Geometric mean: 1.090x faster (HPT: reliability of 96.75%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250611-macm4pro-arm64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.12.6.md)
- [📈time plot](bm-20250611-macm4pro-arm64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.010x faster (HPT: reliability of 76.84%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250611-macm4pro-arm64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.13.0rc2.md)
- [📈time plot](bm-20250611-macm4pro-arm64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.025x slower (HPT: reliability of 99.67%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250611-macm4pro-arm64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-base-mem.svg)
- [📄table](bm-20250611-macm4pro-arm64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-base.md)
- [📈time plot](bm-20250611-macm4pro-arm64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-base.svg)

