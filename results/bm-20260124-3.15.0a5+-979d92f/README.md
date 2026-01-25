# Results

- fork: python/979d92fefc0b6863c978
- version: 3.15.0a5+
- config: 
- commit hash: [979d92f](https://github.com/python/cpython/commit/979d92f)
- commit date: 2026-01-24T16:09:29Z
- commit merge base: [27246c34829ef87adaafafa10e3f946ade7d0de8](https://github.com/python/cpython/commit/27246c34829ef87adaafafa10e3f946ade7d0de8)
- commit date: 2026-01-24T16:09:29+00:00
- ref: 979d92fefc0b6863c978

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21323912132)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20260124-vultr-x86_64-python-979d92fefc0b6863c978-3.15.0a5%2B-979d92f-pystats.json)
- [pystats table](bm-20260124-vultr-x86_64-python-979d92fefc0b6863c978-3.15.0a5%2B-979d92f-pystats.md)
- [raw results](bm-20260124-vultr-x86_64-python-979d92fefc0b6863c978-3.15.0a5%2B-979d92f.json)

### vs. 3.12.6

- Geometric mean: 1.079x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260124-vultr-x86_64-python-979d92fefc0b6863c978-3.15.0a5%2B-979d92f-vs-3.12.6.md)
- [📈time plot](bm-20260124-vultr-x86_64-python-979d92fefc0b6863c978-3.15.0a5%2B-979d92f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.043x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260124-vultr-x86_64-python-979d92fefc0b6863c978-3.15.0a5%2B-979d92f-vs-3.13.0rc2.md)
- [📈time plot](bm-20260124-vultr-x86_64-python-979d92fefc0b6863c978-3.15.0a5%2B-979d92f-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21323912132)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260124-macm4pro-arm64-python-979d92fefc0b6863c978-3.15.0a5%2B-979d92f.json)

### vs. 3.12.6

- Geometric mean: 1.152x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260124-macm4pro-arm64-python-979d92fefc0b6863c978-3.15.0a5%2B-979d92f-vs-3.12.6.md)
- [📈time plot](bm-20260124-macm4pro-arm64-python-979d92fefc0b6863c978-3.15.0a5%2B-979d92f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.069x faster (HPT: reliability of 99.95%, 1.01x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260124-macm4pro-arm64-python-979d92fefc0b6863c978-3.15.0a5%2B-979d92f-vs-3.13.0rc2.md)
- [📈time plot](bm-20260124-macm4pro-arm64-python-979d92fefc0b6863c978-3.15.0a5%2B-979d92f-vs-3.13.0rc2.svg)

