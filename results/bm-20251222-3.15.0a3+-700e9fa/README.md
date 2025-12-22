# Results

- fork: python/700e9fad70da3f1da008
- version: 3.15.0a3+
- config: 
- commit hash: [700e9fa](https://github.com/python/cpython/commit/700e9fa)
- commit date: 2025-12-22T17:10:52+00:00
- commit merge base: [487e91c1203d635c2871541a544a0e6269e50897](https://github.com/python/cpython/commit/487e91c1203d635c2871541a544a0e6269e50897)
- ref: 700e9fad70da3f1da008

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20441405056)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251222-vultr-x86_64-python-700e9fad70da3f1da008-3.15.0a3%2B-700e9fa.json)

### vs. 3.12.6

- Geometric mean: 1.076x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251222-vultr-x86_64-python-700e9fad70da3f1da008-3.15.0a3%2B-700e9fa-vs-3.12.6.md)
- [📈time plot](bm-20251222-vultr-x86_64-python-700e9fad70da3f1da008-3.15.0a3%2B-700e9fa-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.040x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251222-vultr-x86_64-python-700e9fad70da3f1da008-3.15.0a3%2B-700e9fa-vs-3.13.0rc2.md)
- [📈time plot](bm-20251222-vultr-x86_64-python-700e9fad70da3f1da008-3.15.0a3%2B-700e9fa-vs-3.13.0rc2.svg)

