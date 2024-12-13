# Results

- fork: python/ba2d2fda93a03a91ac6c
- version: 3.14.0a2+
- config: 
- commit hash: [ba2d2fd](https://github.com/python/cpython/commit/ba2d2fd)
- commit date: 2024-12-13T05:49:02+08:00
- commit merge base: [0cbc19d59e409854f2b9bdda75e1af2b6cd89ac2](https://github.com/python/cpython/commit/0cbc19d59e409854f2b9bdda75e1af2b6cd89ac2)
- ref: ba2d2fda93a03a91ac6c

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12307195011)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd.json)

### vs. 3.12.6

- Geometric mean: 1.102x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.12.6.md)
- [📈time plot](bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.061x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.13.0rc2.md)
- [📈time plot](bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12307195011)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd.json)

### vs. 3.12.6

- Geometric mean: 1.080x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.12.6.md)
- [📈time plot](bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.042x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.13.0rc2.md)
- [📈time plot](bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.13.0rc2.svg)

