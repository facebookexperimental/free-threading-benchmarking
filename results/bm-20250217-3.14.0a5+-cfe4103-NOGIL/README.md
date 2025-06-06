# Results

- fork: python/cfe41037eb5293a05184
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [cfe4103](https://github.com/python/cpython/commit/cfe4103)
- commit date: 2025-02-17T00:07:10+00:00
- commit merge base: [ae3064608935367c860182dc1b364631082ecdff](https://github.com/python/cpython/commit/ae3064608935367c860182dc1b364631082ecdff)
- ref: cfe41037eb5293a05184

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13360292704)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250217-vultr-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103.json)

### vs. 3.12.6

- Geometric mean: 1.047x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250217-vultr-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-3.12.6.md)
- [📈time plot](bm-20250217-vultr-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.079x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250217-vultr-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-3.13.0rc2.md)
- [📈time plot](bm-20250217-vultr-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.128x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.21x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250217-vultr-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-base-mem.svg)
- [📄table](bm-20250217-vultr-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-base.md)
- [📈time plot](bm-20250217-vultr-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-base.svg)

