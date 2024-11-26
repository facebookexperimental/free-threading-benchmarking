# Results

- fork: python
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [4759ba6](https://github.com/python/cpython/commit/4759ba6)
- commit date: 2024-11-22T12:55:33-05:00
- commit merge base: [8214e0f709010a0e1fa06dc2ce004b5f6103cc6b](https://github.com/python/cpython/commit/8214e0f709010a0e1fa06dc2ce004b5f6103cc6b)
- ref: 4759ba6eec9f0b36b24b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11977743008)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241122-vultr-x86_64-python-4759ba6eec9f0b36b24b-3.14.0a2%2B-4759ba6.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.21x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241122-vultr-x86_64-python-4759ba6eec9f0b36b24b-3.14.0a2%2B-4759ba6-vs-3.12.6.md)
- [📈time plot](bm-20241122-vultr-x86_64-python-4759ba6eec9f0b36b24b-3.14.0a2%2B-4759ba6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.24x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241122-vultr-x86_64-python-4759ba6eec9f0b36b24b-3.14.0a2%2B-4759ba6-vs-3.13.0rc2.md)
- [📈time plot](bm-20241122-vultr-x86_64-python-4759ba6eec9f0b36b24b-3.14.0a2%2B-4759ba6-vs-3.13.0rc2.svg)

