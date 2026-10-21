# Results

- fork: python/a13d6dbe0375670941fa
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [a13d6db](https://github.com/python/cpython/commit/a13d6db)
- commit date: 2026-10-21T18:12:42+00:00
- commit merge base: [65b7e9444a375770208e5282b959fb4e4cc8ed8e](https://github.com/python/cpython/commit/65b7e9444a375770208e5282b959fb4e4cc8ed8e)
- ref: a13d6dbe0375670941fa

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39651451425)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261021-vultr-x86_64-python-a13d6dbe0375670941fa-3.16.0a1%2Bdev-a13d6db.json)

### vs. 3.12.6

- Geometric mean: 1.036x slower (HPT: reliability of 72.41%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261021-vultr-x86_64-python-a13d6dbe0375670941fa-3.16.0a1%2Bdev-a13d6db-vs-3.12.6.md)
- [📈time plot](bm-20261021-vultr-x86_64-python-a13d6dbe0375670941fa-3.16.0a1%2Bdev-a13d6db-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.069x slower (HPT: reliability of 94.31%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261021-vultr-x86_64-python-a13d6dbe0375670941fa-3.16.0a1%2Bdev-a13d6db-vs-3.13.0rc2.md)
- [📈time plot](bm-20261021-vultr-x86_64-python-a13d6dbe0375670941fa-3.16.0a1%2Bdev-a13d6db-vs-3.13.0rc2.svg)

