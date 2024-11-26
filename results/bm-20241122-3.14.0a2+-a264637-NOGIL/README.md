# Results

- fork: python
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [a264637](https://github.com/python/cpython/commit/a264637)
- commit date: 2024-11-22T18:50:30+00:00
- commit merge base: [4759ba6eec9f0b36b24b8eb7e7b120d471c67e82](https://github.com/python/cpython/commit/4759ba6eec9f0b36b24b8eb7e7b120d471c67e82)
- ref: a264637654f9d3ac3c14

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11978619636)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241122-vultr-x86_64-python-a264637654f9d3ac3c14-3.14.0a2%2B-a264637.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.22x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241122-vultr-x86_64-python-a264637654f9d3ac3c14-3.14.0a2%2B-a264637-vs-3.12.6.md)
- [📈time plot](bm-20241122-vultr-x86_64-python-a264637654f9d3ac3c14-3.14.0a2%2B-a264637-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.25x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241122-vultr-x86_64-python-a264637654f9d3ac3c14-3.14.0a2%2B-a264637-vs-3.13.0rc2.md)
- [📈time plot](bm-20241122-vultr-x86_64-python-a264637654f9d3ac3c14-3.14.0a2%2B-a264637-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20241122-vultr-x86_64-python-a264637654f9d3ac3c14-3.14.0a2%2B-a264637-vs-base-mem.svg)
- [📄table](bm-20241122-vultr-x86_64-python-a264637654f9d3ac3c14-3.14.0a2%2B-a264637-vs-base.md)
- [📈time plot](bm-20241122-vultr-x86_64-python-a264637654f9d3ac3c14-3.14.0a2%2B-a264637-vs-base.svg)

