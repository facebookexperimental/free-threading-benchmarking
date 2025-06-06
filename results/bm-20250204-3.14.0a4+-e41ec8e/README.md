# Results

- fork: python/e41ec8e18b078024b02a
- version: 3.14.0a4+
- config: 
- commit hash: [e41ec8e](https://github.com/python/cpython/commit/e41ec8e)
- commit date: 2025-02-04T22:59:23+00:00
- commit merge base: [e5f10a741408206e61cf793451cbd373bbe61594](https://github.com/python/cpython/commit/e5f10a741408206e61cf793451cbd373bbe61594)
- ref: e41ec8e18b078024b02a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13147481780)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e.json)

### vs. 3.12.6

- Geometric mean: 1.092x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.12.6.md)
- [📈time plot](bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.053x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.13.0rc2.svg)

