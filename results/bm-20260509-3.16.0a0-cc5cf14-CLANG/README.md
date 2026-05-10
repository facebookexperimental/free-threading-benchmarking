# Results

- fork: python/cc5cf14ae0a3665ba9d1
- version: 3.16.0a0
- config: CLANG
- commit hash: [cc5cf14](https://github.com/python/cpython/commit/cc5cf14)
- commit date: 2026-05-09T14:39:01-07:00
- commit merge base: [4e97ff3351f381a61b238bd8e805e4e8dd3ea5cf](https://github.com/python/cpython/commit/4e97ff3351f381a61b238bd8e805e4e8dd3ea5cf)
- ref: cc5cf14ae0a3665ba9d1

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25615626552)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json)

### vs. 3.12.6

- Geometric mean: 1.091x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: 2to3, aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14-vs-3.12.6.md)
- [📈time plot](bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.051x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: 2to3, aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14-vs-3.13.0rc2.md)
- [📈time plot](bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.027x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.02x
- [🧠memory plot](bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14-vs-base-mem.svg)
- [📄table](bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14-vs-base.md)
- [📈time plot](bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25615626552)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json)

### vs. 3.12.6

- Geometric mean: 1.137x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14-vs-3.12.6.md)
- [📈time plot](bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.050x faster (HPT: reliability of 98.93%, 1.00x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14-vs-3.13.0rc2.md)
- [📈time plot](bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.024x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14-vs-base-mem.svg)
- [📄table](bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14-vs-base.md)
- [📈time plot](bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14-vs-base.svg)

