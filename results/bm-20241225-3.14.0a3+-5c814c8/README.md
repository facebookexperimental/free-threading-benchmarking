# Results

- fork: python/5c814c83cdd3dc42bd96
- version: 3.14.0a3+
- config: 
- commit hash: [5c814c8](https://github.com/python/cpython/commit/5c814c8)
- commit date: 2024-12-25T19:42:04+02:00
- commit merge base: [81636d3bbd7f126692326bf957707e8a88c91739](https://github.com/python/cpython/commit/81636d3bbd7f126692326bf957707e8a88c91739)
- ref: 5c814c83cdd3dc42bd96

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12497753279)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241225-linux-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8.json)

### vs. 3.12.6

- Geometric mean: 1.100x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241225-linux-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.12.6.md)
- [📈time plot](bm-20241225-linux-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.056x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241225-linux-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.13.0rc2.md)
- [📈time plot](bm-20241225-linux-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12497753279)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241225-vultr-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8.json)

### vs. 3.12.6

- Geometric mean: 1.097x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241225-vultr-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.12.6.md)
- [📈time plot](bm-20241225-vultr-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.058x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241225-vultr-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.13.0rc2.md)
- [📈time plot](bm-20241225-vultr-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.13.0rc2.svg)

