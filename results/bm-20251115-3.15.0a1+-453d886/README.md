# Results

- fork: python/453d886f8592d2f4346d
- version: 3.15.0a1+
- config: 
- commit hash: [453d886](https://github.com/python/cpython/commit/453d886)
- commit date: 2025-11-15T00:13:37Z
- commit merge base: [f0a8bc737ab2f04d4196eee154cb1e17e26ad585](https://github.com/python/cpython/commit/f0a8bc737ab2f04d4196eee154cb1e17e26ad585)
- commit date: 2025-11-15T00:13:37+00:00
- ref: 453d886f8592d2f4346d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19381362498)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251115-vultr-x86_64-python-453d886f8592d2f4346d-3.15.0a1%2B-453d886.json)

### vs. 3.12.6

- Geometric mean: 1.079x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251115-vultr-x86_64-python-453d886f8592d2f4346d-3.15.0a1%2B-453d886-vs-3.12.6.md)
- [📈time plot](bm-20251115-vultr-x86_64-python-453d886f8592d2f4346d-3.15.0a1%2B-453d886-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.043x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251115-vultr-x86_64-python-453d886f8592d2f4346d-3.15.0a1%2B-453d886-vs-3.13.0rc2.md)
- [📈time plot](bm-20251115-vultr-x86_64-python-453d886f8592d2f4346d-3.15.0a1%2B-453d886-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19381362498)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251115-macm4pro-arm64-python-453d886f8592d2f4346d-3.15.0a1%2B-453d886.json)

### vs. 3.12.6

- Geometric mean: 1.140x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251115-macm4pro-arm64-python-453d886f8592d2f4346d-3.15.0a1%2B-453d886-vs-3.12.6.md)
- [📈time plot](bm-20251115-macm4pro-arm64-python-453d886f8592d2f4346d-3.15.0a1%2B-453d886-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.052x faster (HPT: reliability of 99.88%, 1.01x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251115-macm4pro-arm64-python-453d886f8592d2f4346d-3.15.0a1%2B-453d886-vs-3.13.0rc2.md)
- [📈time plot](bm-20251115-macm4pro-arm64-python-453d886f8592d2f4346d-3.15.0a1%2B-453d886-vs-3.13.0rc2.svg)

