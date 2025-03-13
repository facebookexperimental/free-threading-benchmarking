# Results

- fork: python/3618240624d98de2a68a
- version: 3.14.0a5+
- config: 
- commit hash: [3618240](https://github.com/python/cpython/commit/3618240)
- commit date: 2025-03-12T21:45:54+00:00
- commit merge base: [b52866953a64c5e0fe57784fbcfc6bec87861563](https://github.com/python/cpython/commit/b52866953a64c5e0fe57784fbcfc6bec87861563)
- ref: 3618240624d98de2a68a

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13824194042)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250312-linux-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240.json)

### vs. 3.12.6

- Geometric mean: 1.060x faster (HPT: reliability of 99.63%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250312-linux-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.12.6.md)
- [📈time plot](bm-20250312-linux-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.023x faster (HPT: reliability of 89.81%, 1.00x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250312-linux-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.13.0rc2.md)
- [📈time plot](bm-20250312-linux-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13824194042)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250312-vultr-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240.json)

### vs. 3.12.6

- Geometric mean: 1.058x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250312-vultr-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.12.6.md)
- [📈time plot](bm-20250312-vultr-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.019x faster (HPT: reliability of 77.72%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250312-vultr-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.13.0rc2.md)
- [📈time plot](bm-20250312-vultr-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.13.0rc2.svg)

