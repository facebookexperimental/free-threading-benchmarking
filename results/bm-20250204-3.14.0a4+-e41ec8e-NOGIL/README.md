# Results

- fork: python/e41ec8e18b078024b02a
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [e41ec8e](https://github.com/python/cpython/commit/e41ec8e)
- commit date: 2025-02-04T22:59:23+00:00
- commit merge base: [e5f10a741408206e61cf793451cbd373bbe61594](https://github.com/python/cpython/commit/e5f10a741408206e61cf793451cbd373bbe61594)
- ref: e41ec8e18b078024b02a

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13147481780)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250204-linux-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e.json)

### vs. 3.12.6

- Geometric mean: 1.035x slower (HPT: reliability of 99.96%, 1.02x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250204-linux-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.12.6.md)
- [📈time plot](bm-20250204-linux-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.070x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250204-linux-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250204-linux-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.114x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20250204-linux-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-base-mem.svg)
- [📄table](bm-20250204-linux-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-base.md)
- [📈time plot](bm-20250204-linux-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13147481780)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e.json)

### vs. 3.12.6

- Geometric mean: 1.051x slower (HPT: reliability of 99.98%, 1.03x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.12.6.md)
- [📈time plot](bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.081x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.131x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-base-mem.svg)
- [📄table](bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-base.md)
- [📈time plot](bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-base.svg)

