# Results

- fork: python/bef63d2fb81ae2876004
- version: 3.15.0a2+
- config: 
- commit hash: [bef63d2](https://github.com/python/cpython/commit/bef63d2)
- commit date: 2025-12-15T15:18:44-08:00
- commit merge base: [f277781bba684322dffffe45cd878f4652ccf7e4](https://github.com/python/cpython/commit/f277781bba684322dffffe45cd878f4652ccf7e4)
- ref: bef63d2fb81ae2876004

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20252247373)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251215-vultr-x86_64-python-bef63d2fb81ae2876004-3.15.0a2%2B-bef63d2.json)

### vs. 3.12.6

- Geometric mean: 1.072x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251215-vultr-x86_64-python-bef63d2fb81ae2876004-3.15.0a2%2B-bef63d2-vs-3.12.6.md)
- [📈time plot](bm-20251215-vultr-x86_64-python-bef63d2fb81ae2876004-3.15.0a2%2B-bef63d2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.036x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251215-vultr-x86_64-python-bef63d2fb81ae2876004-3.15.0a2%2B-bef63d2-vs-3.13.0rc2.md)
- [📈time plot](bm-20251215-vultr-x86_64-python-bef63d2fb81ae2876004-3.15.0a2%2B-bef63d2-vs-3.13.0rc2.svg)

