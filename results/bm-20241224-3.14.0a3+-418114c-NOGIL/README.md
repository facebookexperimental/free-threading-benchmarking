# Results

- fork: python/418114c139666f33abff
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [418114c](https://github.com/python/cpython/commit/418114c)
- commit date: 2024-12-24T18:29:27+00:00
- commit merge base: [7985d460c731b2c48419a33fc1820f9512bb6f21](https://github.com/python/cpython/commit/7985d460c731b2c48419a33fc1820f9512bb6f21)
- ref: 418114c139666f33abff

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12487494977)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241224-linux-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c.json)

### vs. 3.12.6

- Geometric mean: 1.145x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241224-linux-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.12.6.md)
- [📈time plot](bm-20241224-linux-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.174x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241224-linux-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.13.0rc2.md)
- [📈time plot](bm-20241224-linux-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.224x slower (HPT: reliability of 100.00%, 1.21x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20241224-linux-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-base-mem.svg)
- [📄table](bm-20241224-linux-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-base.md)
- [📈time plot](bm-20241224-linux-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12487494977)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c.json)

### vs. 3.12.6

- Geometric mean: 1.175x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.12.6.md)
- [📈time plot](bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.202x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.13.0rc2.md)
- [📈time plot](bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.234x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-base-mem.svg)
- [📄table](bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-base.md)
- [📈time plot](bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-base.svg)

