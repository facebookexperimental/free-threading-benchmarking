# Results

- fork: python/9e474a98af4184615540
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [9e474a9](https://github.com/python/cpython/commit/9e474a9)
- commit date: 2025-02-26T15:42:39+01:00
- commit merge base: [56e190068177855266f32a7efa329d145b279f94](https://github.com/python/cpython/commit/56e190068177855266f32a7efa329d145b279f94)
- ref: 9e474a98af4184615540

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13550274665)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5%2B-9e474a9.json)

### vs. 3.12.6

- Geometric mean: 1.048x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5%2B-9e474a9-vs-3.12.6.md)
- [📈time plot](bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5%2B-9e474a9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.079x slower (HPT: reliability of 99.99%, 1.06x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5%2B-9e474a9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5%2B-9e474a9-vs-3.13.0rc2.svg)

