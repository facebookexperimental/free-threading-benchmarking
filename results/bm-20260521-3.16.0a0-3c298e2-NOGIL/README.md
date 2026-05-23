# Results

- fork: python/3c298e2e385fc6f462ab
- version: 3.16.0a0
- config: NOGIL
- commit hash: [3c298e2](https://github.com/python/cpython/commit/3c298e2)
- commit date: 2026-05-21T21:44:13+00:00
- commit merge base: [65f99329edf5d0df3ee14d9a242e1a4c8b842211](https://github.com/python/cpython/commit/65f99329edf5d0df3ee14d9a242e1a4c8b842211)
- ref: 3c298e2e385fc6f462ab

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/26262171374)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260521-vultr-x86_64-python-3c298e2e385fc6f462ab-3.16.0a0-3c298e2.json)

### vs. 3.12.6

- Geometric mean: 1.036x slower (HPT: reliability of 91.84%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260521-vultr-x86_64-python-3c298e2e385fc6f462ab-3.16.0a0-3c298e2-vs-3.12.6.md)
- [📈time plot](bm-20260521-vultr-x86_64-python-3c298e2e385fc6f462ab-3.16.0a0-3c298e2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.070x slower (HPT: reliability of 96.58%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260521-vultr-x86_64-python-3c298e2e385fc6f462ab-3.16.0a0-3c298e2-vs-3.13.0rc2.md)
- [📈time plot](bm-20260521-vultr-x86_64-python-3c298e2e385fc6f462ab-3.16.0a0-3c298e2-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.096x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260521-vultr-x86_64-python-3c298e2e385fc6f462ab-3.16.0a0-3c298e2-vs-base-mem.svg)
- [📄table](bm-20260521-vultr-x86_64-python-3c298e2e385fc6f462ab-3.16.0a0-3c298e2-vs-base.md)
- [📈time plot](bm-20260521-vultr-x86_64-python-3c298e2e385fc6f462ab-3.16.0a0-3c298e2-vs-base.svg)

