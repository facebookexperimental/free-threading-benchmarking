# Results

- fork: maurycy/maurycy_tuple_early
- version: 3.15.0a1+
- config: 
- commit hash: [0eae50d](https://github.com/maurycy/cpython/commit/0eae50d)
- commit date: 2025-12-02T13:33:43+01:00
- commit merge base: [1753ccb43223b0a1054aaca31353e3778d2b12a1](https://github.com/python/cpython/commit/1753ccb43223b0a1054aaca31353e3778d2b12a1)
- ref: maurycy_tuple_early

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19966284139)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1%2B-0eae50d.json)

### vs. 3.12.6

- Geometric mean: 1.079x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1%2B-0eae50d-vs-3.12.6.md)
- [📈time plot](bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1%2B-0eae50d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.043x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1%2B-0eae50d-vs-3.13.0rc2.md)
- [📈time plot](bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1%2B-0eae50d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x faster (HPT: reliability of 61.32%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1%2B-0eae50d-vs-base-mem.svg)
- [📄table](bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1%2B-0eae50d-vs-base.md)
- [📈time plot](bm-20251202-vultr-x86_64-maurycy-maurycy_tuple_early-3.15.0a1%2B-0eae50d-vs-base.svg)

