# Results

- fork: python
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [58e334e](https://github.com/python/cpython/commit/58e334e)
- commit date: 2024-11-27T16:14:49+01:00
- commit merge base: [9328db7652677a23192cb51b0324a0fdbfa587c9](https://github.com/python/cpython/commit/9328db7652677a23192cb51b0324a0fdbfa587c9)
- ref: 58e334e1431b2ed6b70e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12059483461)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2%2B-58e334e.json)

### vs. 3.12.6

- Geometric mean: 1.264x slower (HPT: reliability of 100.00%, 1.22x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2%2B-58e334e-vs-3.12.6.md)
- [📈time plot](bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2%2B-58e334e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.289x slower (HPT: reliability of 100.00%, 1.24x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2%2B-58e334e-vs-3.13.0rc2.md)
- [📈time plot](bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2%2B-58e334e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.280x slower (HPT: reliability of 100.00%, 1.24x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: 🔴 sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: html5lib
- [🧠memory plot](bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2%2B-58e334e-vs-base-mem.svg)
- [📄table](bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2%2B-58e334e-vs-base.md)
- [📈time plot](bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2%2B-58e334e-vs-base.svg)

