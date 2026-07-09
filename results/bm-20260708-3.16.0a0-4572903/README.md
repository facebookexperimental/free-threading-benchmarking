# Results

- fork: python/45729033bff28f8abc36
- version: 3.16.0a0
- config: 
- commit hash: [4572903](https://github.com/python/cpython/commit/4572903)
- commit date: 2026-07-08T00:40:54+00:00
- commit merge base: [aa533dce22bf20ba3c1e954aefb245ca1b63543b](https://github.com/python/cpython/commit/aa533dce22bf20ba3c1e954aefb245ca1b63543b)
- ref: 45729033bff28f8abc36

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/28908989456)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260708-vultr-x86_64-python-45729033bff28f8abc36-3.16.0a0-4572903.json)

### vs. 3.12.6

- Geometric mean: 1.074x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260708-vultr-x86_64-python-45729033bff28f8abc36-3.16.0a0-4572903-vs-3.12.6.md)
- [📈time plot](bm-20260708-vultr-x86_64-python-45729033bff28f8abc36-3.16.0a0-4572903-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.037x faster (HPT: reliability of 99.98%, 1.01x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260708-vultr-x86_64-python-45729033bff28f8abc36-3.16.0a0-4572903-vs-3.13.0rc2.md)
- [📈time plot](bm-20260708-vultr-x86_64-python-45729033bff28f8abc36-3.16.0a0-4572903-vs-3.13.0rc2.svg)

