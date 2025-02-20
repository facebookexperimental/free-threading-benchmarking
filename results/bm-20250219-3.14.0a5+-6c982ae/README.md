# Results

- fork: python/6c982aeb547528174f8b
- version: 3.14.0a5+
- config: 
- commit hash: [6c982ae](https://github.com/python/cpython/commit/6c982ae)
- commit date: 2025-02-19T21:44:35+00:00
- commit merge base: [73801864d866c76ae26a120b9db9de21b08f8b50](https://github.com/python/cpython/commit/73801864d866c76ae26a120b9db9de21b08f8b50)
- ref: 6c982aeb547528174f8b

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13425071869)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250219-linux-x86_64-python-6c982aeb547528174f8b-3.14.0a5%2B-6c982ae.json)

### vs. 3.12.6

- Geometric mean: 1.110x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250219-linux-x86_64-python-6c982aeb547528174f8b-3.14.0a5%2B-6c982ae-vs-3.12.6.md)
- [📈time plot](bm-20250219-linux-x86_64-python-6c982aeb547528174f8b-3.14.0a5%2B-6c982ae-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.067x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250219-linux-x86_64-python-6c982aeb547528174f8b-3.14.0a5%2B-6c982ae-vs-3.13.0rc2.md)
- [📈time plot](bm-20250219-linux-x86_64-python-6c982aeb547528174f8b-3.14.0a5%2B-6c982ae-vs-3.13.0rc2.svg)

