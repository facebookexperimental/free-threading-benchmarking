# Results

- fork: python/354ef336e4cd48cf0c02
- version: 3.16.0a0
- config: NOGIL
- commit hash: [354ef33](https://github.com/python/cpython/commit/354ef33)
- commit date: 2026-05-09T01:01:35+01:00
- commit merge base: [45c47d26c230086163ac1ef0aa9f955f794fb69c](https://github.com/python/cpython/commit/45c47d26c230086163ac1ef0aa9f955f794fb69c)
- ref: 354ef336e4cd48cf0c02

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25586883686)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260509-vultr-x86_64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33.json)

### vs. 3.12.6

- Geometric mean: 1.042x slower (HPT: reliability of 93.72%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260509-vultr-x86_64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33-vs-3.12.6.md)
- [📈time plot](bm-20260509-vultr-x86_64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.076x slower (HPT: reliability of 97.53%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260509-vultr-x86_64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33-vs-3.13.0rc2.md)
- [📈time plot](bm-20260509-vultr-x86_64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.108x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260509-vultr-x86_64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33-vs-base-mem.svg)
- [📄table](bm-20260509-vultr-x86_64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33-vs-base.md)
- [📈time plot](bm-20260509-vultr-x86_64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25586883686)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33.json)

### vs. 3.12.6

- Geometric mean: 1.095x faster (HPT: reliability of 99.72%, 1.00x faster at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33-vs-3.12.6.md)
- [📈time plot](bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.011x faster (HPT: reliability of 66.15%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33-vs-3.13.0rc2.md)
- [📈time plot](bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.024x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33-vs-base-mem.svg)
- [📄table](bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33-vs-base.md)
- [📈time plot](bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33-vs-base.svg)

