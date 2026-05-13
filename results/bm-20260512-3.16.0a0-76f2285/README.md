# Results

- fork: python/76f22853410d3ded872c
- version: 3.16.0a0
- config: 
- commit hash: [76f2285](https://github.com/python/cpython/commit/76f2285)
- commit date: 2026-05-12T23:46:21Z
- commit merge base: [9eb3b1466865f6fa7821b194e96204bd056a2c53](https://github.com/python/cpython/commit/9eb3b1466865f6fa7821b194e96204bd056a2c53)
- commit date: 2026-05-12T23:46:21+00:00
- ref: 76f22853410d3ded872c

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25771399397)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260512-vultr-x86_64-python-76f22853410d3ded872c-3.16.0a0-76f2285.json)

### vs. 3.12.6

- Geometric mean: 1.061x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260512-vultr-x86_64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.12.6.md)
- [📈time plot](bm-20260512-vultr-x86_64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.023x faster (HPT: reliability of 99.60%, 1.00x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260512-vultr-x86_64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.13.0rc2.md)
- [📈time plot](bm-20260512-vultr-x86_64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25771399397)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260512-macm4pro-arm64-python-76f22853410d3ded872c-3.16.0a0-76f2285.json)

### vs. 3.12.6

- Geometric mean: 1.136x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260512-macm4pro-arm64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.12.6.md)
- [📈time plot](bm-20260512-macm4pro-arm64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.049x faster (HPT: reliability of 99.88%, 1.00x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260512-macm4pro-arm64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.13.0rc2.md)
- [📈time plot](bm-20260512-macm4pro-arm64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.13.0rc2.svg)

