# Results

- fork: python/ec91e1c2762412f1408b
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [ec91e1c](https://github.com/python/cpython/commit/ec91e1c)
- commit date: 2025-01-23T16:53:53+01:00
- commit merge base: [cf0b2da1e6947aa15be119582c2017765ab46863](https://github.com/python/cpython/commit/cf0b2da1e6947aa15be119582c2017765ab46863)
- ref: ec91e1c2762412f1408b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12934444280)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250123-vultr-x86_64-python-ec91e1c2762412f1408b-3.14.0a4%2B-ec91e1c.json)

### vs. 3.12.6

- Geometric mean: 1.057x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250123-vultr-x86_64-python-ec91e1c2762412f1408b-3.14.0a4%2B-ec91e1c-vs-3.12.6.md)
- [📈time plot](bm-20250123-vultr-x86_64-python-ec91e1c2762412f1408b-3.14.0a4%2B-ec91e1c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.088x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250123-vultr-x86_64-python-ec91e1c2762412f1408b-3.14.0a4%2B-ec91e1c-vs-3.13.0rc2.md)
- [📈time plot](bm-20250123-vultr-x86_64-python-ec91e1c2762412f1408b-3.14.0a4%2B-ec91e1c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.137x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250123-vultr-x86_64-python-ec91e1c2762412f1408b-3.14.0a4%2B-ec91e1c-vs-base-mem.svg)
- [📄table](bm-20250123-vultr-x86_64-python-ec91e1c2762412f1408b-3.14.0a4%2B-ec91e1c-vs-base.md)
- [📈time plot](bm-20250123-vultr-x86_64-python-ec91e1c2762412f1408b-3.14.0a4%2B-ec91e1c-vs-base.svg)

