# Results

- fork: python/49918f5b0ceb1950c322
- version: 3.16.0a0
- config: NOGIL
- commit hash: [49918f5](https://github.com/python/cpython/commit/49918f5)
- commit date: 2026-05-07T23:02:04Z
- commit merge base: [b142878db1e54149feba62b08df1236432793bf0](https://github.com/python/cpython/commit/b142878db1e54149feba62b08df1236432793bf0)
- commit date: 2026-05-07T23:02:04+00:00
- ref: 49918f5b0ceb1950c322

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25530387328)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260507-vultr-x86_64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5.json)

### vs. 3.12.6

- Geometric mean: 1.037x slower (HPT: reliability of 85.81%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260507-vultr-x86_64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.12.6.md)
- [📈time plot](bm-20260507-vultr-x86_64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.072x slower (HPT: reliability of 98.05%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260507-vultr-x86_64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.13.0rc2.md)
- [📈time plot](bm-20260507-vultr-x86_64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.090x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260507-vultr-x86_64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-base-mem.svg)
- [📄table](bm-20260507-vultr-x86_64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-base.md)
- [📈time plot](bm-20260507-vultr-x86_64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25530387328)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260507-macm4pro-arm64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5.json)

### vs. 3.12.6

- Geometric mean: 1.090x faster (HPT: reliability of 99.38%, 1.00x faster at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260507-macm4pro-arm64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.12.6.md)
- [📈time plot](bm-20260507-macm4pro-arm64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.006x faster (HPT: reliability of 76.86%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260507-macm4pro-arm64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.13.0rc2.md)
- [📈time plot](bm-20260507-macm4pro-arm64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.022x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260507-macm4pro-arm64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-base-mem.svg)
- [📄table](bm-20260507-macm4pro-arm64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-base.md)
- [📈time plot](bm-20260507-macm4pro-arm64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-base.svg)

