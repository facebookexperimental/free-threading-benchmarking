# Results

- fork: python/548c7314138b85cab3b9
- version: 3.16.0a0
- config: 
- commit hash: [548c731](https://github.com/python/cpython/commit/548c731)
- commit date: 2026-07-03T14:01:58-07:00
- commit merge base: [cde31ec135905472f1137dddcc8227af2430d89c](https://github.com/python/cpython/commit/cde31ec135905472f1137dddcc8227af2430d89c)
- ref: 548c7314138b85cab3b9

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/28689745658)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260703-vultr-x86_64-python-548c7314138b85cab3b9-3.16.0a0-548c731.json)

### vs. 3.12.6

- Geometric mean: 1.073x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260703-vultr-x86_64-python-548c7314138b85cab3b9-3.16.0a0-548c731-vs-3.12.6.md)
- [📈time plot](bm-20260703-vultr-x86_64-python-548c7314138b85cab3b9-3.16.0a0-548c731-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.037x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260703-vultr-x86_64-python-548c7314138b85cab3b9-3.16.0a0-548c731-vs-3.13.0rc2.md)
- [📈time plot](bm-20260703-vultr-x86_64-python-548c7314138b85cab3b9-3.16.0a0-548c731-vs-3.13.0rc2.svg)

