# Results

- fork: python/ee68f5f46a14e2bbf22d
- version: 3.16.0a0
- config: NOGIL
- commit hash: [ee68f5f](https://github.com/python/cpython/commit/ee68f5f)
- commit date: 2026-08-11T23:16:05+00:00
- commit merge base: [3444ef9d30e0d4160357ab93109407d1ed377635](https://github.com/python/cpython/commit/3444ef9d30e0d4160357ab93109407d1ed377635)
- ref: ee68f5f46a14e2bbf22d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/31550346905)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f.json)

### vs. 3.12.6

- Geometric mean: 1.030x slower (HPT: reliability of 77.02%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f-vs-3.12.6.md)
- [📈time plot](bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.062x slower (HPT: reliability of 92.74%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f-vs-3.13.0rc2.md)
- [📈time plot](bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.097x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f-vs-base-mem.svg)
- [📄table](bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f-vs-base.md)
- [📈time plot](bm-20260811-vultr-x86_64-python-ee68f5f46a14e2bbf22d-3.16.0a0-ee68f5f-vs-base.svg)

