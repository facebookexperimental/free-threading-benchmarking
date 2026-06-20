# Results

- fork: python/d701f8edbe2884e3e039
- version: 3.16.0a0
- config: NOGIL
- commit hash: [d701f8e](https://github.com/python/cpython/commit/d701f8e)
- commit date: 2026-06-19T07:29:33+08:00
- commit merge base: [17720b184d333c7a869d801ed1a56cd91f42bdc2](https://github.com/python/cpython/commit/17720b184d333c7a869d801ed1a56cd91f42bdc2)
- ref: d701f8edbe2884e3e039

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/27799349240)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260619-vultr-x86_64-python-d701f8edbe2884e3e039-3.16.0a0-d701f8e.json)

### vs. 3.12.6

- Geometric mean: 1.033x slower (HPT: reliability of 87.56%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260619-vultr-x86_64-python-d701f8edbe2884e3e039-3.16.0a0-d701f8e-vs-3.12.6.md)
- [📈time plot](bm-20260619-vultr-x86_64-python-d701f8edbe2884e3e039-3.16.0a0-d701f8e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.066x slower (HPT: reliability of 97.03%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260619-vultr-x86_64-python-d701f8edbe2884e3e039-3.16.0a0-d701f8e-vs-3.13.0rc2.md)
- [📈time plot](bm-20260619-vultr-x86_64-python-d701f8edbe2884e3e039-3.16.0a0-d701f8e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.110x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260619-vultr-x86_64-python-d701f8edbe2884e3e039-3.16.0a0-d701f8e-vs-base-mem.svg)
- [📄table](bm-20260619-vultr-x86_64-python-d701f8edbe2884e3e039-3.16.0a0-d701f8e-vs-base.md)
- [📈time plot](bm-20260619-vultr-x86_64-python-d701f8edbe2884e3e039-3.16.0a0-d701f8e-vs-base.svg)

