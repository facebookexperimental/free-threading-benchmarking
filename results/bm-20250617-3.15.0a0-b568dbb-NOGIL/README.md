# Results

- fork: nascheme/gh_133136_qsbr_defer
- version: 3.15.0a0
- config: NOGIL
- commit hash: [b568dbb](https://github.com/nascheme/cpython/commit/b568dbb)
- commit date: 2025-06-17T11:53:49-07:00
- commit merge base: [fba5dded6df3c2b1943557afef89a5cb418f65a2](https://github.com/python/cpython/commit/fba5dded6df3c2b1943557afef89a5cb418f65a2)
- ref: gh_133136_qsbr_defer

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15716179933)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb.json)

### vs. 3.12.6

- Geometric mean: 1.017x faster (HPT: reliability of 77.28%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb-vs-3.12.6.md)
- [📈time plot](bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.018x slower (HPT: reliability of 94.65%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb-vs-3.13.0rc2.md)
- [📈time plot](bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x faster (HPT: reliability of 99.91%, 1.00x faster at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb-vs-base-mem.svg)
- [📄table](bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb-vs-base.md)
- [📈time plot](bm-20250617-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-b568dbb-vs-base.svg)

