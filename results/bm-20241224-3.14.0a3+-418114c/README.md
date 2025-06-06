# Results

- fork: python/418114c139666f33abff
- version: 3.14.0a3+
- config: 
- commit hash: [418114c](https://github.com/python/cpython/commit/418114c)
- commit date: 2024-12-24T18:29:27+00:00
- commit merge base: [7985d460c731b2c48419a33fc1820f9512bb6f21](https://github.com/python/cpython/commit/7985d460c731b2c48419a33fc1820f9512bb6f21)
- ref: 418114c139666f33abff

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12487494977)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c.json)

### vs. 3.12.6

- Geometric mean: 1.084x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.12.6.md)
- [📈time plot](bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.046x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.13.0rc2.md)
- [📈time plot](bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.13.0rc2.svg)

