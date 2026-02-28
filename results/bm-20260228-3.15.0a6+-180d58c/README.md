# Results

- fork: python/180d58cbcc0f7f34d6ba
- version: 3.15.0a6+
- config: 
- commit hash: [180d58c](https://github.com/python/cpython/commit/180d58c)
- commit date: 2026-02-28T00:23:12+00:00
- commit merge base: [72eca2af59043c78647b0e6be3777a947ea9ef0f](https://github.com/python/cpython/commit/72eca2af59043c78647b0e6be3777a947ea9ef0f)
- ref: 180d58cbcc0f7f34d6ba

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22509287348)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6%2B-180d58c.json)

### vs. 3.12.6

- Geometric mean: 1.070x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6%2B-180d58c-vs-3.12.6.md)
- [📈time plot](bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6%2B-180d58c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.034x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6%2B-180d58c-vs-3.13.0rc2.md)
- [📈time plot](bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6%2B-180d58c-vs-3.13.0rc2.svg)

