# Results

- fork: python/e8092e5cdcd6707ac0b1
- version: 3.14.0a4+
- config: 
- commit hash: [e8092e5](https://github.com/python/cpython/commit/e8092e5)
- commit date: 2025-01-18T20:52:30+00:00
- commit merge base: [fba475ae6f932d0aaee6832b4102b2d4c50df70f](https://github.com/python/cpython/commit/fba475ae6f932d0aaee6832b4102b2d4c50df70f)
- ref: e8092e5cdcd6707ac0b1

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12847971419)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250118-vultr-x86_64-python-e8092e5cdcd6707ac0b1-3.14.0a4%2B-e8092e5.json)

### vs. 3.12.6

- Geometric mean: 1.096x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250118-vultr-x86_64-python-e8092e5cdcd6707ac0b1-3.14.0a4%2B-e8092e5-vs-3.12.6.md)
- [📈time plot](bm-20250118-vultr-x86_64-python-e8092e5cdcd6707ac0b1-3.14.0a4%2B-e8092e5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.057x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250118-vultr-x86_64-python-e8092e5cdcd6707ac0b1-3.14.0a4%2B-e8092e5-vs-3.13.0rc2.md)
- [📈time plot](bm-20250118-vultr-x86_64-python-e8092e5cdcd6707ac0b1-3.14.0a4%2B-e8092e5-vs-3.13.0rc2.svg)

