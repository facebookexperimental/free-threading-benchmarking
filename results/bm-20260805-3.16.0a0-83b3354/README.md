# Results

- fork: python/83b33546b9c68578dda7
- version: 3.16.0a0
- config: 
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

- Geometric mean: 1.067x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260805-vultr-x86_64-python-83b33546b9c68578dda7-3.16.0a0-83b3354-vs-3.12.6.md)
- [📈time plot](bm-20260805-vultr-x86_64-python-83b33546b9c68578dda7-3.16.0a0-83b3354-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.032x faster (HPT: reliability of 99.92%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260805-vultr-x86_64-python-83b33546b9c68578dda7-3.16.0a0-83b3354-vs-3.13.0rc2.md)
- [📈time plot](bm-20260805-vultr-x86_64-python-83b33546b9c68578dda7-3.16.0a0-83b3354-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x faster (HPT: reliability of 61.30%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20260805-vultr-x86_64-python-83b33546b9c68578dda7-3.16.0a0-83b3354-vs-base-mem.svg)
- [📄table](bm-20260805-vultr-x86_64-python-83b33546b9c68578dda7-3.16.0a0-83b3354-vs-base.md)
- [📈time plot](bm-20260805-vultr-x86_64-python-83b33546b9c68578dda7-3.16.0a0-83b3354-vs-base.svg)

