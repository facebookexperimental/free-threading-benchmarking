# Results

- fork: python/6b5511d66bab0754d1d9
- version: 3.15.0a7+
- config: NOGIL
- commit hash: [6b5511d](https://github.com/python/cpython/commit/6b5511d)
- commit date: 2026-03-19T22:14:13Z
- commit merge base: [98977ca4334b7f7738ff2ed9238616143a1dc69e](https://github.com/python/cpython/commit/98977ca4334b7f7738ff2ed9238616143a1dc69e)
- commit date: 2026-03-19T22:14:13+00:00
- ref: 6b5511d66bab0754d1d9

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23323818861)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260319-vultr-x86_64-python-6b5511d66bab0754d1d9-3.15.0a7%2B-6b5511d.json)

### vs. 3.12.6

- Geometric mean: 1.027x slower (HPT: reliability of 85.43%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260319-vultr-x86_64-python-6b5511d66bab0754d1d9-3.15.0a7%2B-6b5511d-vs-3.12.6.md)
- [📈time plot](bm-20260319-vultr-x86_64-python-6b5511d66bab0754d1d9-3.15.0a7%2B-6b5511d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.061x slower (HPT: reliability of 89.81%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260319-vultr-x86_64-python-6b5511d66bab0754d1d9-3.15.0a7%2B-6b5511d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260319-vultr-x86_64-python-6b5511d66bab0754d1d9-3.15.0a7%2B-6b5511d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.091x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20260319-vultr-x86_64-python-6b5511d66bab0754d1d9-3.15.0a7%2B-6b5511d-vs-base-mem.svg)
- [📄table](bm-20260319-vultr-x86_64-python-6b5511d66bab0754d1d9-3.15.0a7%2B-6b5511d-vs-base.md)
- [📈time plot](bm-20260319-vultr-x86_64-python-6b5511d66bab0754d1d9-3.15.0a7%2B-6b5511d-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23323818861)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260319-macm4pro-arm64-python-6b5511d66bab0754d1d9-3.15.0a7%2B-6b5511d.json)

### vs. 3.12.6

- Geometric mean: 1.097x faster (HPT: reliability of 99.64%, 1.00x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260319-macm4pro-arm64-python-6b5511d66bab0754d1d9-3.15.0a7%2B-6b5511d-vs-3.12.6.md)
- [📈time plot](bm-20260319-macm4pro-arm64-python-6b5511d66bab0754d1d9-3.15.0a7%2B-6b5511d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.018x faster (HPT: reliability of 52.52%, 1.00x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260319-macm4pro-arm64-python-6b5511d66bab0754d1d9-3.15.0a7%2B-6b5511d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260319-macm4pro-arm64-python-6b5511d66bab0754d1d9-3.15.0a7%2B-6b5511d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.026x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260319-macm4pro-arm64-python-6b5511d66bab0754d1d9-3.15.0a7%2B-6b5511d-vs-base-mem.svg)
- [📄table](bm-20260319-macm4pro-arm64-python-6b5511d66bab0754d1d9-3.15.0a7%2B-6b5511d-vs-base.md)
- [📈time plot](bm-20260319-macm4pro-arm64-python-6b5511d66bab0754d1d9-3.15.0a7%2B-6b5511d-vs-base.svg)

