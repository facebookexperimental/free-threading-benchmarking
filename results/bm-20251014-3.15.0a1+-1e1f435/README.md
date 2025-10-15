# Results

- fork: python/1e1f43519605b7c54a96
- version: 3.15.0a1+
- config: 
- commit hash: [1e1f435](https://github.com/python/cpython/commit/1e1f435)
- commit date: 2025-10-14T23:34:30+00:00
- commit merge base: [2ca3c85054b231505c5e6f5f3209eb5f63942dce](https://github.com/python/cpython/commit/2ca3c85054b231505c5e6f5f3209eb5f63942dce)
- ref: 1e1f43519605b7c54a96

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18513864742)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251014-vultr-x86_64-python-1e1f43519605b7c54a96-3.15.0a1%2B-1e1f435.json)

### vs. 3.12.6

- Geometric mean: 1.071x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251014-vultr-x86_64-python-1e1f43519605b7c54a96-3.15.0a1%2B-1e1f435-vs-3.12.6.md)
- [📈time plot](bm-20251014-vultr-x86_64-python-1e1f43519605b7c54a96-3.15.0a1%2B-1e1f435-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.035x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251014-vultr-x86_64-python-1e1f43519605b7c54a96-3.15.0a1%2B-1e1f435-vs-3.13.0rc2.md)
- [📈time plot](bm-20251014-vultr-x86_64-python-1e1f43519605b7c54a96-3.15.0a1%2B-1e1f435-vs-3.13.0rc2.svg)

