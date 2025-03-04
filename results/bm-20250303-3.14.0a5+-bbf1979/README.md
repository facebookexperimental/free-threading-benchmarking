# Results

- fork: python/bbf197913ca984b79fee
- version: 3.14.0a5+
- config: 
- commit hash: [bbf1979](https://github.com/python/cpython/commit/bbf1979)
- commit date: 2025-03-03T14:58:33-08:00
- commit merge base: [3a7f17c7e2f72a836a019c316818c446a0c71d75](https://github.com/python/cpython/commit/3a7f17c7e2f72a836a019c316818c446a0c71d75)
- ref: bbf197913ca984b79fee

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13643350016)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250303-linux-x86_64-python-bbf197913ca984b79fee-3.14.0a5%2B-bbf1979.json)

### vs. 3.12.6

- Geometric mean: 1.114x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250303-linux-x86_64-python-bbf197913ca984b79fee-3.14.0a5%2B-bbf1979-vs-3.12.6.md)
- [📈time plot](bm-20250303-linux-x86_64-python-bbf197913ca984b79fee-3.14.0a5%2B-bbf1979-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250303-linux-x86_64-python-bbf197913ca984b79fee-3.14.0a5%2B-bbf1979-vs-3.13.0rc2.md)
- [📈time plot](bm-20250303-linux-x86_64-python-bbf197913ca984b79fee-3.14.0a5%2B-bbf1979-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13643350016)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250303-vultr-x86_64-python-bbf197913ca984b79fee-3.14.0a5%2B-bbf1979.json)

### vs. 3.12.6

- Geometric mean: 1.110x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250303-vultr-x86_64-python-bbf197913ca984b79fee-3.14.0a5%2B-bbf1979-vs-3.12.6.md)
- [📈time plot](bm-20250303-vultr-x86_64-python-bbf197913ca984b79fee-3.14.0a5%2B-bbf1979-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.069x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250303-vultr-x86_64-python-bbf197913ca984b79fee-3.14.0a5%2B-bbf1979-vs-3.13.0rc2.md)
- [📈time plot](bm-20250303-vultr-x86_64-python-bbf197913ca984b79fee-3.14.0a5%2B-bbf1979-vs-3.13.0rc2.svg)

