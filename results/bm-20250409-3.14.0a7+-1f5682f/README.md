# Results

- fork: python/1f5682f3a27516833f7c
- version: 3.14.0a7+
- config: 
- commit hash: [1f5682f](https://github.com/python/cpython/commit/1f5682f)
- commit date: 2025-04-09T10:34:12-07:00
- commit merge base: [67ded6a4faae29edff8e4f7886978e71ce116e33](https://github.com/python/cpython/commit/67ded6a4faae29edff8e4f7886978e71ce116e33)
- ref: 1f5682f3a27516833f7c

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14363652904)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7%2B-1f5682f.json)

### vs. 3.12.6

- Geometric mean: 1.124x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7%2B-1f5682f-vs-3.12.6.md)
- [📈time plot](bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7%2B-1f5682f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.084x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7%2B-1f5682f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250409-vultr-x86_64-python-1f5682f3a27516833f7c-3.14.0a7%2B-1f5682f-vs-3.13.0rc2.svg)

