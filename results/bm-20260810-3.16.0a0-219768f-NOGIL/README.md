# Results

- fork: python/219768ff531fc0686de6
- version: 3.16.0a0
- config: NOGIL
- commit hash: [219768f](https://github.com/python/cpython/commit/219768f)
- commit date: 2026-08-10T21:44:50+02:00
- commit merge base: [7571c41da7505e6b551dae305b285af2a9139771](https://github.com/python/cpython/commit/7571c41da7505e6b551dae305b285af2a9139771)
- ref: 219768ff531fc0686de6

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/31445911278)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260810-vultr-x86_64-python-219768ff531fc0686de6-3.16.0a0-219768f.json)

### vs. 3.12.6

- Geometric mean: 1.041x slower (HPT: reliability of 90.02%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260810-vultr-x86_64-python-219768ff531fc0686de6-3.16.0a0-219768f-vs-3.12.6.md)
- [📈time plot](bm-20260810-vultr-x86_64-python-219768ff531fc0686de6-3.16.0a0-219768f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.073x slower (HPT: reliability of 99.68%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260810-vultr-x86_64-python-219768ff531fc0686de6-3.16.0a0-219768f-vs-3.13.0rc2.md)
- [📈time plot](bm-20260810-vultr-x86_64-python-219768ff531fc0686de6-3.16.0a0-219768f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.105x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20260810-vultr-x86_64-python-219768ff531fc0686de6-3.16.0a0-219768f-vs-base-mem.svg)
- [📄table](bm-20260810-vultr-x86_64-python-219768ff531fc0686de6-3.16.0a0-219768f-vs-base.md)
- [📈time plot](bm-20260810-vultr-x86_64-python-219768ff531fc0686de6-3.16.0a0-219768f-vs-base.svg)

