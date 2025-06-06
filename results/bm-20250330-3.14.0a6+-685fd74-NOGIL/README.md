# Results

- fork: python/685fd74f81e673dc0430
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [685fd74](https://github.com/python/cpython/commit/685fd74)
- commit date: 2025-03-30T16:07:25-07:00
- commit merge base: [39fa19a4ccb4c75d2421187e5b8d83c73b48ca4d](https://github.com/python/cpython/commit/39fa19a4ccb4c75d2421187e5b8d83c73b48ca4d)
- ref: 685fd74f81e673dc0430

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14161514757)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250330-vultr-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74.json)

### vs. 3.12.6

- Geometric mean: 1.092x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250330-vultr-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.12.6.md)
- [📈time plot](bm-20250330-vultr-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.122x slower (HPT: reliability of 99.99%, 1.08x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250330-vultr-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.13.0rc2.md)
- [📈time plot](bm-20250330-vultr-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.185x slower (HPT: reliability of 100.00%, 1.17x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250330-vultr-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-base-mem.svg)
- [📄table](bm-20250330-vultr-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-base.md)
- [📈time plot](bm-20250330-vultr-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14161514757)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250330-macm4pro-arm64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74.json)

### vs. 3.12.6

- Geometric mean: 1.005x faster (HPT: reliability of 95.22%, 1.00x slower at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250330-macm4pro-arm64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.12.6.md)
- [📈time plot](bm-20250330-macm4pro-arm64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.068x slower (HPT: reliability of 99.85%, 1.02x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250330-macm4pro-arm64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.13.0rc2.md)
- [📈time plot](bm-20250330-macm4pro-arm64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.036x slower (HPT: reliability of 99.91%, 1.01x slower at 99th %ile)
- Memory usage: 1.10x
- [🧠memory plot](bm-20250330-macm4pro-arm64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-base-mem.svg)
- [📄table](bm-20250330-macm4pro-arm64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-base.md)
- [📈time plot](bm-20250330-macm4pro-arm64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-base.svg)

