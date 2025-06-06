# Results

- fork: python/ec91e1c2762412f1408b
- version: 3.14.0a4+
- config: 
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

- Geometric mean: 1.092x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250123-vultr-x86_64-python-ec91e1c2762412f1408b-3.14.0a4%2B-ec91e1c-vs-3.12.6.md)
- [📈time plot](bm-20250123-vultr-x86_64-python-ec91e1c2762412f1408b-3.14.0a4%2B-ec91e1c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.054x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250123-vultr-x86_64-python-ec91e1c2762412f1408b-3.14.0a4%2B-ec91e1c-vs-3.13.0rc2.md)
- [📈time plot](bm-20250123-vultr-x86_64-python-ec91e1c2762412f1408b-3.14.0a4%2B-ec91e1c-vs-3.13.0rc2.svg)

