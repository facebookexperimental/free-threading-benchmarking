# Results

- fork: python/c75d220e257ef7fda8d5
- version: 3.15.0a7+
- config: NOGIL
- commit hash: [c75d220](https://github.com/python/cpython/commit/c75d220)
- commit date: 2026-03-26T23:40:32+01:00
- commit merge base: [ca6dfa0f31132c80aaad40855087c2d931dc2d0f](https://github.com/python/cpython/commit/ca6dfa0f31132c80aaad40855087c2d931dc2d0f)
- ref: c75d220e257ef7fda8d5

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23625288496)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260326-vultr-x86_64-python-c75d220e257ef7fda8d5-3.15.0a7%2B-c75d220.json)

### vs. 3.12.6

- Geometric mean: 1.028x slower (HPT: reliability of 79.80%, 1.00x slower at 99th %ile)
- Memory usage: 1.44x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260326-vultr-x86_64-python-c75d220e257ef7fda8d5-3.15.0a7%2B-c75d220-vs-3.12.6.md)
- [📈time plot](bm-20260326-vultr-x86_64-python-c75d220e257ef7fda8d5-3.15.0a7%2B-c75d220-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.060x slower (HPT: reliability of 88.84%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260326-vultr-x86_64-python-c75d220e257ef7fda8d5-3.15.0a7%2B-c75d220-vs-3.13.0rc2.md)
- [📈time plot](bm-20260326-vultr-x86_64-python-c75d220e257ef7fda8d5-3.15.0a7%2B-c75d220-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.093x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260326-vultr-x86_64-python-c75d220e257ef7fda8d5-3.15.0a7%2B-c75d220-vs-base-mem.svg)
- [📄table](bm-20260326-vultr-x86_64-python-c75d220e257ef7fda8d5-3.15.0a7%2B-c75d220-vs-base.md)
- [📈time plot](bm-20260326-vultr-x86_64-python-c75d220e257ef7fda8d5-3.15.0a7%2B-c75d220-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23625288496)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7%2B-c75d220.json)

### vs. 3.12.6

- Geometric mean: 1.101x faster (HPT: reliability of 99.65%, 1.00x faster at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7%2B-c75d220-vs-3.12.6.md)
- [📈time plot](bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7%2B-c75d220-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.021x faster (HPT: reliability of 61.39%, 1.00x faster at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7%2B-c75d220-vs-3.13.0rc2.md)
- [📈time plot](bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7%2B-c75d220-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.056x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7%2B-c75d220-vs-base-mem.svg)
- [📄table](bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7%2B-c75d220-vs-base.md)
- [📈time plot](bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7%2B-c75d220-vs-base.svg)

