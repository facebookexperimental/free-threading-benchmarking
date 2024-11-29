# Results

- fork: python
- version: 3.14.0a2+
- config: 
- commit hash: [b83be9c](https://github.com/python/cpython/commit/b83be9c)
- commit date: 2024-11-28T19:03:09+02:00
- commit merge base: [20657fbdb14d50ca4ec115da0cbef155871d8d33](https://github.com/python/cpython/commit/20657fbdb14d50ca4ec115da0cbef155871d8d33)
- ref: b83be9c9718aac42d0d8

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12076969482)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241128-linux-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c.json)

### vs. 3.12.6

- Geometric mean: 1.061x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241128-linux-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c-vs-3.12.6.md)
- [📈time plot](bm-20241128-linux-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.019x faster (HPT: reliability of 99.84%, 1.00x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241128-linux-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c-vs-3.13.0rc2.md)
- [📈time plot](bm-20241128-linux-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12076969482)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241128-vultr-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c.json)

### vs. 3.12.6

- Geometric mean: 1.040x faster (HPT: reliability of 99.93%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241128-vultr-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c-vs-3.12.6.md)
- [📈time plot](bm-20241128-vultr-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.002x faster (HPT: reliability of 50.91%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241128-vultr-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c-vs-3.13.0rc2.md)
- [📈time plot](bm-20241128-vultr-x86_64-python-b83be9c9718aac42d0d8-3.14.0a2%2B-b83be9c-vs-3.13.0rc2.svg)

