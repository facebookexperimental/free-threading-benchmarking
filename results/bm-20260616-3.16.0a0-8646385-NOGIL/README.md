# Results

- fork: python/8646385076ea4f6ef086
- version: 3.16.0a0
- config: NOGIL
- commit hash: [8646385](https://github.com/python/cpython/commit/8646385)
- commit date: 2026-06-16T06:16:16+08:00
- commit merge base: [5ea1e907d1928c1e08cf4246e8935d62a95ca8a1](https://github.com/python/cpython/commit/5ea1e907d1928c1e08cf4246e8935d62a95ca8a1)
- ref: 8646385076ea4f6ef086

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/27587351740)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260616-vultr-x86_64-python-8646385076ea4f6ef086-3.16.0a0-8646385.json)

### vs. 3.12.6

- Geometric mean: 1.034x slower (HPT: reliability of 87.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260616-vultr-x86_64-python-8646385076ea4f6ef086-3.16.0a0-8646385-vs-3.12.6.md)
- [📈time plot](bm-20260616-vultr-x86_64-python-8646385076ea4f6ef086-3.16.0a0-8646385-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.067x slower (HPT: reliability of 97.50%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260616-vultr-x86_64-python-8646385076ea4f6ef086-3.16.0a0-8646385-vs-3.13.0rc2.md)
- [📈time plot](bm-20260616-vultr-x86_64-python-8646385076ea4f6ef086-3.16.0a0-8646385-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.101x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260616-vultr-x86_64-python-8646385076ea4f6ef086-3.16.0a0-8646385-vs-base-mem.svg)
- [📄table](bm-20260616-vultr-x86_64-python-8646385076ea4f6ef086-3.16.0a0-8646385-vs-base.md)
- [📈time plot](bm-20260616-vultr-x86_64-python-8646385076ea4f6ef086-3.16.0a0-8646385-vs-base.svg)

