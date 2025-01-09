# Results

- fork: python/a1284e97979ff73ad72a
- version: 3.14.0a3+
- config: 
- commit hash: [a1284e9](https://github.com/python/cpython/commit/a1284e9)
- commit date: 2025-01-08T18:38:02-05:00
- commit merge base: [58a9133fc2caea15d11116f0b5bd6832374cb88c](https://github.com/python/cpython/commit/58a9133fc2caea15d11116f0b5bd6832374cb88c)
- ref: a1284e97979ff73ad72a

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12681442983)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3%2B-a1284e9.json)

### vs. 3.12.6

- Geometric mean: 1.098x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3%2B-a1284e9-vs-3.12.6.md)
- [📈time plot](bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3%2B-a1284e9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x faster (HPT: reliability of 99.94%, 1.01x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3%2B-a1284e9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3%2B-a1284e9-vs-3.13.0rc2.svg)

