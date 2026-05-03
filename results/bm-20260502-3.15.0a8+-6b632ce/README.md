# Results

- fork: python/6b632ce36b950c7753c5
- version: 3.15.0a8+
- config: 
- commit hash: [6b632ce](https://github.com/python/cpython/commit/6b632ce)
- commit date: 2026-05-02T13:28:00-07:00
- commit merge base: [7c9ad27dd1fc9e05149b471b055f18ad64cd05f3](https://github.com/python/cpython/commit/7c9ad27dd1fc9e05149b471b055f18ad64cd05f3)
- ref: 6b632ce36b950c7753c5

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25265686339)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20260502-vultr-x86_64-python-6b632ce36b950c7753c5-3.15.0a8%2B-6b632ce-pystats.json)
- [pystats table](bm-20260502-vultr-x86_64-python-6b632ce36b950c7753c5-3.15.0a8%2B-6b632ce-pystats.md)
- [raw results](bm-20260502-vultr-x86_64-python-6b632ce36b950c7753c5-3.15.0a8%2B-6b632ce.json)

### vs. 3.12.6

- Geometric mean: 1.056x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260502-vultr-x86_64-python-6b632ce36b950c7753c5-3.15.0a8%2B-6b632ce-vs-3.12.6.md)
- [📈time plot](bm-20260502-vultr-x86_64-python-6b632ce36b950c7753c5-3.15.0a8%2B-6b632ce-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.021x faster (HPT: reliability of 99.96%, 1.01x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260502-vultr-x86_64-python-6b632ce36b950c7753c5-3.15.0a8%2B-6b632ce-vs-3.13.0rc2.md)
- [📈time plot](bm-20260502-vultr-x86_64-python-6b632ce36b950c7753c5-3.15.0a8%2B-6b632ce-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25265686339)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260502-macm4pro-arm64-python-6b632ce36b950c7753c5-3.15.0a8%2B-6b632ce.json)

### vs. 3.12.6

- Geometric mean: 1.133x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260502-macm4pro-arm64-python-6b632ce36b950c7753c5-3.15.0a8%2B-6b632ce-vs-3.12.6.md)
- [📈time plot](bm-20260502-macm4pro-arm64-python-6b632ce36b950c7753c5-3.15.0a8%2B-6b632ce-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.050x faster (HPT: reliability of 99.96%, 1.00x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260502-macm4pro-arm64-python-6b632ce36b950c7753c5-3.15.0a8%2B-6b632ce-vs-3.13.0rc2.md)
- [📈time plot](bm-20260502-macm4pro-arm64-python-6b632ce36b950c7753c5-3.15.0a8%2B-6b632ce-vs-3.13.0rc2.svg)

