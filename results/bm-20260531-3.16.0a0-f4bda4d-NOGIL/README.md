# Results

- fork: python/f4bda4d6cb13d4c57fba
- version: 3.16.0a0
- config: NOGIL
- commit hash: [f4bda4d](https://github.com/python/cpython/commit/f4bda4d)
- commit date: 2026-05-31T20:28:02+01:00
- commit merge base: [2f8f569ba911ab3cff1356a15a3e688adc4ae917](https://github.com/python/cpython/commit/2f8f569ba911ab3cff1356a15a3e688adc4ae917)
- ref: f4bda4d6cb13d4c57fba

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/26729938923)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d.json)

### vs. 3.12.6

- Geometric mean: 1.030x slower (HPT: reliability of 85.45%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d-vs-3.12.6.md)
- [📈time plot](bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.066x slower (HPT: reliability of 96.37%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.091x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d-vs-base-mem.svg)
- [📄table](bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d-vs-base.md)
- [📈time plot](bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d-vs-base.svg)

