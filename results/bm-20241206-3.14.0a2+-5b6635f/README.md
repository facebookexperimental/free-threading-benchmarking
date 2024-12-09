# Results

- fork: python/5b6635f772d187d6049a
- version: 3.14.0a2+
- config: 
- commit hash: [5b6635f](https://github.com/python/cpython/commit/5b6635f)
- commit date: 2024-12-06T18:10:00+00:00
- commit merge base: [e59caf67cdb8dae26470f00599ea8dbb00968a73](https://github.com/python/cpython/commit/e59caf67cdb8dae26470f00599ea8dbb00968a73)
- ref: 5b6635f772d187d6049a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12242759347)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241206-vultr-x86_64-python-5b6635f772d187d6049a-3.14.0a2%2B-5b6635f.json)

### vs. 3.12.6

- Geometric mean: 1.067x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241206-vultr-x86_64-python-5b6635f772d187d6049a-3.14.0a2%2B-5b6635f-vs-3.12.6.md)
- [📈time plot](bm-20241206-vultr-x86_64-python-5b6635f772d187d6049a-3.14.0a2%2B-5b6635f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.029x faster (HPT: reliability of 94.84%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241206-vultr-x86_64-python-5b6635f772d187d6049a-3.14.0a2%2B-5b6635f-vs-3.13.0rc2.md)
- [📈time plot](bm-20241206-vultr-x86_64-python-5b6635f772d187d6049a-3.14.0a2%2B-5b6635f-vs-3.13.0rc2.svg)

