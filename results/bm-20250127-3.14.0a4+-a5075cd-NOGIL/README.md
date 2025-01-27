# Results

- fork: python/a5075cd5bd0307d9c19a
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [a5075cd](https://github.com/python/cpython/commit/a5075cd)
- commit date: 2025-01-27T16:36:09+02:00
- commit merge base: [9546fe2ef2db921709f3cb355b33bba977658672](https://github.com/python/cpython/commit/9546fe2ef2db921709f3cb355b33bba977658672)
- ref: a5075cd5bd0307d9c19a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12993576813)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250127-vultr-x86_64-python-a5075cd5bd0307d9c19a-3.14.0a4%2B-a5075cd.json)

### vs. 3.12.6

- Geometric mean: 1.071x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250127-vultr-x86_64-python-a5075cd5bd0307d9c19a-3.14.0a4%2B-a5075cd-vs-3.12.6.md)
- [📈time plot](bm-20250127-vultr-x86_64-python-a5075cd5bd0307d9c19a-3.14.0a4%2B-a5075cd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.101x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250127-vultr-x86_64-python-a5075cd5bd0307d9c19a-3.14.0a4%2B-a5075cd-vs-3.13.0rc2.md)
- [📈time plot](bm-20250127-vultr-x86_64-python-a5075cd5bd0307d9c19a-3.14.0a4%2B-a5075cd-vs-3.13.0rc2.svg)

