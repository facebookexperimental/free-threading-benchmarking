# Results

- fork: python/a7160912274003672dc1
- version: 3.15.0a1+
- config: JIT
- commit hash: [a716091](https://github.com/python/cpython/commit/a716091)
- commit date: 2025-10-27T18:26:47+00:00
- commit merge base: [0f0a362768aecb4c791724cce486d8317533a94d](https://github.com/python/cpython/commit/0f0a362768aecb4c791724cce486d8317533a94d)
- ref: a7160912274003672dc1

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18859814110)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1%2B-a716091.json)

### vs. 3.12.6

- Geometric mean: 1.088x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1%2B-a716091-vs-3.12.6.md)
- [📈time plot](bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1%2B-a716091-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.052x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1%2B-a716091-vs-3.13.0rc2.md)
- [📈time plot](bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1%2B-a716091-vs-3.13.0rc2.svg)

