# Results

- fork: python/5dbe2ac850b7b180685e
- version: 3.16.0a2+dev
- config: NOGIL
- commit hash: [5dbe2ac](https://github.com/python/cpython/commit/5dbe2ac)
- commit date: 2026-11-27T00:15:39+01:00
- commit merge base: [ff9803a617a3a4d42f5ce9c1ea2cb3bf224766ef](https://github.com/python/cpython/commit/ff9803a617a3a4d42f5ce9c1ea2cb3bf224766ef)
- ref: 5dbe2ac850b7b180685e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/45916603941)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261127-vultr-x86_64-python-5dbe2ac850b7b180685e-3.16.0a2%2Bdev-5dbe2ac.json)

### vs. 3.12.6

- Geometric mean: 1.015x slower (HPT: reliability of 55.45%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261127-vultr-x86_64-python-5dbe2ac850b7b180685e-3.16.0a2%2Bdev-5dbe2ac-vs-3.12.6.md)
- [📈time plot](bm-20261127-vultr-x86_64-python-5dbe2ac850b7b180685e-3.16.0a2%2Bdev-5dbe2ac-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.049x slower (HPT: reliability of 82.22%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261127-vultr-x86_64-python-5dbe2ac850b7b180685e-3.16.0a2%2Bdev-5dbe2ac-vs-3.13.0rc2.md)
- [📈time plot](bm-20261127-vultr-x86_64-python-5dbe2ac850b7b180685e-3.16.0a2%2Bdev-5dbe2ac-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.106x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.14x
- [🧠memory plot](bm-20261127-vultr-x86_64-python-5dbe2ac850b7b180685e-3.16.0a2%2Bdev-5dbe2ac-vs-base-mem.svg)
- [📄table](bm-20261127-vultr-x86_64-python-5dbe2ac850b7b180685e-3.16.0a2%2Bdev-5dbe2ac-vs-base.md)
- [📈time plot](bm-20261127-vultr-x86_64-python-5dbe2ac850b7b180685e-3.16.0a2%2Bdev-5dbe2ac-vs-base.svg)

