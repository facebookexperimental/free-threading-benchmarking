# Results

- fork: python/bca35f0e782848ae2acd
- version: 3.14.0a4+
- config: 
- commit hash: [bca35f0](https://github.com/python/cpython/commit/bca35f0)
- commit date: 2025-01-20T00:05:22+00:00
- commit merge base: [3b6a27c5607d2b199f127c2a5ef5316bbc30ae42](https://github.com/python/cpython/commit/3b6a27c5607d2b199f127c2a5ef5316bbc30ae42)
- ref: bca35f0e782848ae2acd

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12858552253)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0.json)

### vs. 3.12.6

- Geometric mean: 1.072x faster (HPT: reliability of 99.81%, 1.01x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0-vs-3.12.6.md)
- [📈time plot](bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.029x faster (HPT: reliability of 99.33%, 1.00x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12858552253)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0.json)

### vs. 3.12.6

- Geometric mean: 1.093x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0-vs-3.12.6.md)
- [📈time plot](bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0-vs-3.13.0rc2.svg)

