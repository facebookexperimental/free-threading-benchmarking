# Results

- fork: python/1b41c7b722b77d9c02c6
- version: 3.16.0a0
- config: NOGIL
- commit hash: [1b41c7b](https://github.com/python/cpython/commit/1b41c7b)
- commit date: 2026-07-10T01:29:53+02:00
- commit merge base: [87e5aac5ec85939cbd7623c0d7b4acc3cffd14ef](https://github.com/python/cpython/commit/87e5aac5ec85939cbd7623c0d7b4acc3cffd14ef)
- ref: 1b41c7b722b77d9c02c6

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/29060823660)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260710-vultr-x86_64-python-1b41c7b722b77d9c02c6-3.16.0a0-1b41c7b.json)

### vs. 3.12.6

- Geometric mean: 1.036x slower (HPT: reliability of 91.81%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260710-vultr-x86_64-python-1b41c7b722b77d9c02c6-3.16.0a0-1b41c7b-vs-3.12.6.md)
- [📈time plot](bm-20260710-vultr-x86_64-python-1b41c7b722b77d9c02c6-3.16.0a0-1b41c7b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.068x slower (HPT: reliability of 98.03%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260710-vultr-x86_64-python-1b41c7b722b77d9c02c6-3.16.0a0-1b41c7b-vs-3.13.0rc2.md)
- [📈time plot](bm-20260710-vultr-x86_64-python-1b41c7b722b77d9c02c6-3.16.0a0-1b41c7b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.105x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260710-vultr-x86_64-python-1b41c7b722b77d9c02c6-3.16.0a0-1b41c7b-vs-base-mem.svg)
- [📄table](bm-20260710-vultr-x86_64-python-1b41c7b722b77d9c02c6-3.16.0a0-1b41c7b-vs-base.md)
- [📈time plot](bm-20260710-vultr-x86_64-python-1b41c7b722b77d9c02c6-3.16.0a0-1b41c7b-vs-base.svg)

