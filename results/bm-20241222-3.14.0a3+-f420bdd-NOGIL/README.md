# Results

- fork: python/f420bdd29fbc1a97ad20
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [f420bdd](https://github.com/python/cpython/commit/f420bdd)
- commit date: 2024-12-22T18:34:16+02:00
- commit merge base: [b66a4ad9fc32b63da2ba10db24cbc8f4e29f781a](https://github.com/python/cpython/commit/b66a4ad9fc32b63da2ba10db24cbc8f4e29f781a)
- ref: f420bdd29fbc1a97ad20

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12456412425)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3%2B-f420bdd.json)

### vs. 3.12.6

- Geometric mean: 1.187x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3%2B-f420bdd-vs-3.12.6.md)
- [📈time plot](bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3%2B-f420bdd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.213x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3%2B-f420bdd-vs-3.13.0rc2.md)
- [📈time plot](bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3%2B-f420bdd-vs-3.13.0rc2.svg)

