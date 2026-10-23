# Results

- fork: python/5b55b502221b67660a4d
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [5b55b50](https://github.com/python/cpython/commit/5b55b50)
- commit date: 2026-10-22T21:35:18+00:00
- commit merge base: [c6796a1268292bca0711b05557130ba3406f9850](https://github.com/python/cpython/commit/c6796a1268292bca0711b05557130ba3406f9850)
- ref: 5b55b502221b67660a4d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39860993693)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261022-vultr-x86_64-python-5b55b502221b67660a4d-3.16.0a1%2Bdev-5b55b50.json)

### vs. 3.12.6

- Geometric mean: 1.039x slower (HPT: reliability of 71.58%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261022-vultr-x86_64-python-5b55b502221b67660a4d-3.16.0a1%2Bdev-5b55b50-vs-3.12.6.md)
- [📈time plot](bm-20261022-vultr-x86_64-python-5b55b502221b67660a4d-3.16.0a1%2Bdev-5b55b50-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.071x slower (HPT: reliability of 98.44%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261022-vultr-x86_64-python-5b55b502221b67660a4d-3.16.0a1%2Bdev-5b55b50-vs-3.13.0rc2.md)
- [📈time plot](bm-20261022-vultr-x86_64-python-5b55b502221b67660a4d-3.16.0a1%2Bdev-5b55b50-vs-3.13.0rc2.svg)

