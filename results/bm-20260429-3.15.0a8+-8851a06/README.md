# Results

- fork: python/8851a06e6e7ff23d91e5
- version: 3.15.0a8+
- config: 
- commit hash: [8851a06](https://github.com/python/cpython/commit/8851a06)
- commit date: 2026-04-29T18:33:05+03:00
- commit merge base: [025a82f138b9a59c2cb842aaa8835206f0879b20](https://github.com/python/cpython/commit/025a82f138b9a59c2cb842aaa8835206f0879b20)
- ref: 8851a06e6e7ff23d91e5

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25141706282)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06.json)

### vs. 3.12.6

- Geometric mean: 1.087x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.12.6.md)
- [📈time plot](bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.051x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.13.0rc2.md)
- [📈time plot](bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25141706282)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260429-macm4pro-arm64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06.json)

### vs. 3.12.6

- Geometric mean: 1.187x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260429-macm4pro-arm64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.12.6.md)
- [📈time plot](bm-20260429-macm4pro-arm64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.100x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260429-macm4pro-arm64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.13.0rc2.md)
- [📈time plot](bm-20260429-macm4pro-arm64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.13.0rc2.svg)

