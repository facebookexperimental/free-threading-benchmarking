# Results

- fork: python/5dd775bed086909722ec
- version: 3.14.0a2+
- config: 
- commit hash: [5dd775b](https://github.com/python/cpython/commit/5dd775b)
- commit date: 2024-12-13T17:21:46+01:00
- commit merge base: [8bc18182a7c28f86265c9d82bd0338137480921c](https://github.com/python/cpython/commit/8bc18182a7c28f86265c9d82bd0338137480921c)
- ref: 5dd775bed086909722ec

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12322649011)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2%2B-5dd775b.json)

### vs. 3.12.6

- Geometric mean: 1.083x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2%2B-5dd775b-vs-3.12.6.md)
- [📈time plot](bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2%2B-5dd775b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.044x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2%2B-5dd775b-vs-3.13.0rc2.md)
- [📈time plot](bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2%2B-5dd775b-vs-3.13.0rc2.svg)

