# Results

- fork: python/8b3cccf3f9508572d85b
- version: 3.14.0a2+
- config: 
- commit hash: [8b3cccf](https://github.com/python/cpython/commit/8b3cccf)
- commit date: 2024-12-05T21:39:43+00:00
- commit merge base: [f4f530804b9d8f089eba0f157ec2144c03b13651](https://github.com/python/cpython/commit/f4f530804b9d8f089eba0f157ec2144c03b13651)
- ref: 8b3cccf3f9508572d85b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12190496848)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241205-vultr-x86_64-python-8b3cccf3f9508572d85b-3.14.0a2%2B-8b3cccf.json)

### vs. 3.12.6

- Geometric mean: 1.066x faster (HPT: reliability of 99.98%, 1.01x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241205-vultr-x86_64-python-8b3cccf3f9508572d85b-3.14.0a2%2B-8b3cccf-vs-3.12.6.md)
- [📈time plot](bm-20241205-vultr-x86_64-python-8b3cccf3f9508572d85b-3.14.0a2%2B-8b3cccf-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.028x faster (HPT: reliability of 78.79%, 1.00x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241205-vultr-x86_64-python-8b3cccf3f9508572d85b-3.14.0a2%2B-8b3cccf-vs-3.13.0rc2.md)
- [📈time plot](bm-20241205-vultr-x86_64-python-8b3cccf3f9508572d85b-3.14.0a2%2B-8b3cccf-vs-3.13.0rc2.svg)

