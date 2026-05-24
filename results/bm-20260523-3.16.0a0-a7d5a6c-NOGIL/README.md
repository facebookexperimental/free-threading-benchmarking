# Results

- fork: python/a7d5a6cc179e2eabd780
- version: 3.16.0a0
- config: NOGIL
- commit hash: [a7d5a6c](https://github.com/python/cpython/commit/a7d5a6c)
- commit date: 2026-05-23T00:04:51+02:00
- commit merge base: [9df2b6ccc719b0bc0167da65b72b57f9da39398b](https://github.com/python/cpython/commit/9df2b6ccc719b0bc0167da65b72b57f9da39398b)
- ref: a7d5a6cc179e2eabd780

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/26319117109)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c.json)

### vs. 3.12.6

- Geometric mean: 1.031x slower (HPT: reliability of 83.31%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c-vs-3.12.6.md)
- [📈time plot](bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.066x slower (HPT: reliability of 95.50%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c-vs-3.13.0rc2.md)
- [📈time plot](bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.097x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c-vs-base-mem.svg)
- [📄table](bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c-vs-base.md)
- [📈time plot](bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c-vs-base.svg)

