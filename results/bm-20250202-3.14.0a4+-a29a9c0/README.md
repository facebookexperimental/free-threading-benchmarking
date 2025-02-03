# Results

- fork: python/a29a9c0f3890fec843b7
- version: 3.14.0a4+
- config: 
- commit hash: [a29a9c0](https://github.com/python/cpython/commit/a29a9c0)
- commit date: 2025-02-02T15:19:55-08:00
- commit merge base: [567394517a10c9a9f3af25a31009589ae2c50f1b](https://github.com/python/cpython/commit/567394517a10c9a9f3af25a31009589ae2c50f1b)
- ref: a29a9c0f3890fec843b7

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13103920156)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250202-linux-x86_64-python-a29a9c0f3890fec843b7-3.14.0a4%2B-a29a9c0.json)

### vs. 3.12.6

- Geometric mean: 1.096x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250202-linux-x86_64-python-a29a9c0f3890fec843b7-3.14.0a4%2B-a29a9c0-vs-3.12.6.md)
- [📈time plot](bm-20250202-linux-x86_64-python-a29a9c0f3890fec843b7-3.14.0a4%2B-a29a9c0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.054x faster (HPT: reliability of 99.98%, 1.02x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250202-linux-x86_64-python-a29a9c0f3890fec843b7-3.14.0a4%2B-a29a9c0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250202-linux-x86_64-python-a29a9c0f3890fec843b7-3.14.0a4%2B-a29a9c0-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13103920156)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250202-vultr-x86_64-python-a29a9c0f3890fec843b7-3.14.0a4%2B-a29a9c0.json)

### vs. 3.12.6

- Geometric mean: 1.101x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250202-vultr-x86_64-python-a29a9c0f3890fec843b7-3.14.0a4%2B-a29a9c0-vs-3.12.6.md)
- [📈time plot](bm-20250202-vultr-x86_64-python-a29a9c0f3890fec843b7-3.14.0a4%2B-a29a9c0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.062x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250202-vultr-x86_64-python-a29a9c0f3890fec843b7-3.14.0a4%2B-a29a9c0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250202-vultr-x86_64-python-a29a9c0f3890fec843b7-3.14.0a4%2B-a29a9c0-vs-3.13.0rc2.svg)

