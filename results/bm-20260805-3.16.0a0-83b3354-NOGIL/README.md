# Results

- fork: python/83b33546b9c68578dda7
- version: 3.16.0a0
- config: NOGIL
- commit hash: [83b3354](https://github.com/python/cpython/commit/83b3354)
- commit date: 2026-08-05T06:02:49+08:00
- commit merge base: [30ac23e3e413c2d38b80691b1c80e3cd74a22639](https://github.com/python/cpython/commit/30ac23e3e413c2d38b80691b1c80e3cd74a22639)
- ref: 83b33546b9c68578dda7

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/30964001796)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260805-vultr-x86_64-python-83b33546b9c68578dda7-3.16.0a0-83b3354.json)

### vs. 3.12.6

- Geometric mean: 1.038x slower (HPT: reliability of 92.46%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260805-vultr-x86_64-python-83b33546b9c68578dda7-3.16.0a0-83b3354-vs-3.12.6.md)
- [📈time plot](bm-20260805-vultr-x86_64-python-83b33546b9c68578dda7-3.16.0a0-83b3354-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.070x slower (HPT: reliability of 97.10%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260805-vultr-x86_64-python-83b33546b9c68578dda7-3.16.0a0-83b3354-vs-3.13.0rc2.md)
- [📈time plot](bm-20260805-vultr-x86_64-python-83b33546b9c68578dda7-3.16.0a0-83b3354-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x slower (HPT: reliability of 62.57%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20260805-vultr-x86_64-python-83b33546b9c68578dda7-3.16.0a0-83b3354-vs-base-mem.svg)
- [📄table](bm-20260805-vultr-x86_64-python-83b33546b9c68578dda7-3.16.0a0-83b3354-vs-base.md)
- [📈time plot](bm-20260805-vultr-x86_64-python-83b33546b9c68578dda7-3.16.0a0-83b3354-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.101x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [📄table](bm-20260805-vultr-x86_64-python-83b33546b9c68578dda7-3.16.0a0-83b3354-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20260805-vultr-x86_64-python-83b33546b9c68578dda7-3.16.0a0-83b3354-vs-default_base_vs_NOGIL.svg)

