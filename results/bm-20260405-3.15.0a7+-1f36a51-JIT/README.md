# Results

- fork: python/1f36a510a2a16e8ff155
- version: 3.15.0a7+
- config: JIT
- commit hash: [1f36a51](https://github.com/python/cpython/commit/1f36a51)
- commit date: 2026-04-05T00:31:54+02:00
- commit merge base: [4ff8b07a3d907c5a755a862a86496ed6c6fb2f3d](https://github.com/python/cpython/commit/4ff8b07a3d907c5a755a862a86496ed6c6fb2f3d)
- ref: 1f36a510a2a16e8ff155

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23990660009)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260405-vultr-x86_64-python-1f36a510a2a16e8ff155-3.15.0a7%2B-1f36a51.json)

### vs. 3.12.6

- Geometric mean: 1.166x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260405-vultr-x86_64-python-1f36a510a2a16e8ff155-3.15.0a7%2B-1f36a51-vs-3.12.6.md)
- [📈time plot](bm-20260405-vultr-x86_64-python-1f36a510a2a16e8ff155-3.15.0a7%2B-1f36a51-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.128x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260405-vultr-x86_64-python-1f36a510a2a16e8ff155-3.15.0a7%2B-1f36a51-vs-3.13.0rc2.md)
- [📈time plot](bm-20260405-vultr-x86_64-python-1f36a510a2a16e8ff155-3.15.0a7%2B-1f36a51-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.082x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20260405-vultr-x86_64-python-1f36a510a2a16e8ff155-3.15.0a7%2B-1f36a51-vs-base-mem.svg)
- [📄table](bm-20260405-vultr-x86_64-python-1f36a510a2a16e8ff155-3.15.0a7%2B-1f36a51-vs-base.md)
- [📈time plot](bm-20260405-vultr-x86_64-python-1f36a510a2a16e8ff155-3.15.0a7%2B-1f36a51-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23990660009)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260405-macm4pro-arm64-python-1f36a510a2a16e8ff155-3.15.0a7%2B-1f36a51.json)

### vs. 3.12.6

- Geometric mean: 1.268x faster (HPT: reliability of 100.00%, 1.13x faster at 99th %ile)
- Memory usage: 1.28x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260405-macm4pro-arm64-python-1f36a510a2a16e8ff155-3.15.0a7%2B-1f36a51-vs-3.12.6.md)
- [📈time plot](bm-20260405-macm4pro-arm64-python-1f36a510a2a16e8ff155-3.15.0a7%2B-1f36a51-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.176x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260405-macm4pro-arm64-python-1f36a510a2a16e8ff155-3.15.0a7%2B-1f36a51-vs-3.13.0rc2.md)
- [📈time plot](bm-20260405-macm4pro-arm64-python-1f36a510a2a16e8ff155-3.15.0a7%2B-1f36a51-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.095x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20260405-macm4pro-arm64-python-1f36a510a2a16e8ff155-3.15.0a7%2B-1f36a51-vs-base-mem.svg)
- [📄table](bm-20260405-macm4pro-arm64-python-1f36a510a2a16e8ff155-3.15.0a7%2B-1f36a51-vs-base.md)
- [📈time plot](bm-20260405-macm4pro-arm64-python-1f36a510a2a16e8ff155-3.15.0a7%2B-1f36a51-vs-base.svg)

