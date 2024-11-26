# Results

- fork: python
- version: 3.14.0a2+
- config: 
- commit hash: [17c16ae](https://github.com/python/cpython/commit/17c16ae)
- commit date: 2024-11-24T14:42:50-08:00
- commit merge base: [307c63358681d669ae39e5ecd814bded4a93443a](https://github.com/python/cpython/commit/307c63358681d669ae39e5ecd814bded4a93443a)
- ref: 17c16aea66b606d66f71

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12000941135)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241124-linux-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae.json)

### vs. 3.12.6

- Geometric mean: 1.091x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241124-linux-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.12.6.md)
- [📈time plot](bm-20241124-linux-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.047x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241124-linux-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.13.0rc2.md)
- [📈time plot](bm-20241124-linux-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12000941135)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae.json)

### vs. 3.12.6

- Geometric mean: 1.032x faster (HPT: reliability of 99.93%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.12.6.md)
- [📈time plot](bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.005x slower (HPT: reliability of 90.14%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.13.0rc2.md)
- [📈time plot](bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.13.0rc2.svg)

