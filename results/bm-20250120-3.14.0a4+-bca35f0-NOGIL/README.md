# Results

- fork: python/bca35f0e782848ae2acd
- version: 3.14.0a4+
- config: NOGIL
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

- Geometric mean: 1.073x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0-vs-3.12.6.md)
- [📈time plot](bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.107x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.127x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0-vs-base-mem.svg)
- [📄table](bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0-vs-base.md)
- [📈time plot](bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12858552253)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0.json)

### vs. 3.12.6

- Geometric mean: 1.058x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0-vs-3.12.6.md)
- [📈time plot](bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.089x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.139x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0-vs-base-mem.svg)
- [📄table](bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0-vs-base.md)
- [📈time plot](bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4%2B-bca35f0-vs-base.svg)

