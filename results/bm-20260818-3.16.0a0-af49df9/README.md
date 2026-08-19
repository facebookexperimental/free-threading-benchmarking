# Results

- fork: python/af49df919dafc3767ae9
- version: 3.16.0a0
- config: 
- commit hash: [af49df9](https://github.com/python/cpython/commit/af49df9)
- commit date: 2026-08-18T19:55:57+01:00
- commit merge base: [c5168eadf15665310b22ff44e23738034d3e5036](https://github.com/python/cpython/commit/c5168eadf15665310b22ff44e23738034d3e5036)
- ref: af49df919dafc3767ae9

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/32200623196)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9.json)

### vs. 3.12.6

- Geometric mean: 1.072x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.12.6.md)
- [📈time plot](bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.037x faster (HPT: reliability of 99.97%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.13.0rc2.md)
- [📈time plot](bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/32200623196)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9.json)

### vs. 3.12.6

- Geometric mean: 1.131x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.12.6.md)
- [📈time plot](bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.044x faster (HPT: reliability of 97.78%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.13.0rc2.md)
- [📈time plot](bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.13.0rc2.svg)

