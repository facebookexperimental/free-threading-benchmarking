# Results

- fork: python/05e89c34bd8389f87bd6
- version: 3.14.0a5+
- config: 
- commit hash: [05e89c3](https://github.com/python/cpython/commit/05e89c3)
- commit date: 2025-02-13T10:51:03-08:00
- commit merge base: [07f5e33f2eed50984d7a60b48bb3136d93a59dd6](https://github.com/python/cpython/commit/07f5e33f2eed50984d7a60b48bb3136d93a59dd6)
- ref: 05e89c34bd8389f87bd6

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13319755959)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250213-linux-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5%2B-05e89c3.json)

### vs. 3.12.6

- Geometric mean: 1.124x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250213-linux-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5%2B-05e89c3-vs-3.12.6.md)
- [📈time plot](bm-20250213-linux-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5%2B-05e89c3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.079x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250213-linux-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5%2B-05e89c3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250213-linux-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5%2B-05e89c3-vs-3.13.0rc2.svg)

