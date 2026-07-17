# Results

- fork: python/b4662e8e3b60a2644861
- version: 3.16.0a0
- config: NOGIL
- commit hash: [b4662e8](https://github.com/python/cpython/commit/b4662e8)
- commit date: 2026-07-15T20:05:17+02:00
- commit merge base: [681477de459bd12ab2429669aa6d52cbed83c018](https://github.com/python/cpython/commit/681477de459bd12ab2429669aa6d52cbed83c018)
- ref: b4662e8e3b60a2644861

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/29462072884)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260715-vultr-x86_64-python-b4662e8e3b60a2644861-3.16.0a0-b4662e8.json)

### vs. 3.12.6

- Geometric mean: 1.047x slower (HPT: reliability of 98.28%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260715-vultr-x86_64-python-b4662e8e3b60a2644861-3.16.0a0-b4662e8-vs-3.12.6.md)
- [📈time plot](bm-20260715-vultr-x86_64-python-b4662e8e3b60a2644861-3.16.0a0-b4662e8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.078x slower (HPT: reliability of 99.95%, 1.01x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260715-vultr-x86_64-python-b4662e8e3b60a2644861-3.16.0a0-b4662e8-vs-3.13.0rc2.md)
- [📈time plot](bm-20260715-vultr-x86_64-python-b4662e8e3b60a2644861-3.16.0a0-b4662e8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.113x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260715-vultr-x86_64-python-b4662e8e3b60a2644861-3.16.0a0-b4662e8-vs-base-mem.svg)
- [📄table](bm-20260715-vultr-x86_64-python-b4662e8e3b60a2644861-3.16.0a0-b4662e8-vs-base.md)
- [📈time plot](bm-20260715-vultr-x86_64-python-b4662e8e3b60a2644861-3.16.0a0-b4662e8-vs-base.svg)

