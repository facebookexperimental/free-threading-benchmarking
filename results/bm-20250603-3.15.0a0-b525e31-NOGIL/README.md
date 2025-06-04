# Results

- fork: python/b525e31b7fc50e7a498f
- version: 3.15.0a0
- config: NOGIL
- commit hash: [b525e31](https://github.com/python/cpython/commit/b525e31)
- commit date: 2025-06-03T08:40:40+09:00
- commit merge base: [0ac9e17fb47075c9446b99da4dffe4cad993b97a](https://github.com/python/cpython/commit/0ac9e17fb47075c9446b99da4dffe4cad993b97a)
- ref: b525e31b7fc50e7a498f

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15405686953)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250603-vultr-x86_64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31.json)

### vs. 3.12.6

- Geometric mean: 1.013x faster (HPT: reliability of 90.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250603-vultr-x86_64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.12.6.md)
- [📈time plot](bm-20250603-vultr-x86_64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.022x slower (HPT: reliability of 95.57%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250603-vultr-x86_64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.13.0rc2.md)
- [📈time plot](bm-20250603-vultr-x86_64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.092x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250603-vultr-x86_64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-base-mem.svg)
- [📄table](bm-20250603-vultr-x86_64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-base.md)
- [📈time plot](bm-20250603-vultr-x86_64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15405686953)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31.json)

### vs. 3.12.6

- Geometric mean: 1.100x faster (HPT: reliability of 99.17%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.12.6.md)
- [📈time plot](bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.019x faster (HPT: reliability of 59.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.13.0rc2.md)
- [📈time plot](bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.021x slower (HPT: reliability of 98.49%, 1.00x slower at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-base-mem.svg)
- [📄table](bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-base.md)
- [📈time plot](bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-base.svg)

