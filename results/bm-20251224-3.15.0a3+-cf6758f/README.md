# Results

- fork: python/cf6758ff9ebd6df8ac2a
- version: 3.15.0a3+
- config: 
- commit hash: [cf6758f](https://github.com/python/cpython/commit/cf6758f)
- commit date: 2025-12-24T22:03:00Z
- commit merge base: [594a4631c3afd4139b6783f15034a92878c8eff1](https://github.com/python/cpython/commit/594a4631c3afd4139b6783f15034a92878c8eff1)
- commit date: 2025-12-24T22:03:00+00:00
- ref: cf6758ff9ebd6df8ac2a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20496171456)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f.json)

### vs. 3.12.6

- Geometric mean: 1.077x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.12.6.md)
- [📈time plot](bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.041x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.13.0rc2.md)
- [📈time plot](bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20496171456)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f.json)

### vs. 3.12.6

- Geometric mean: 1.163x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.12.6.md)
- [📈time plot](bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.078x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.13.0rc2.md)
- [📈time plot](bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.13.0rc2.svg)

