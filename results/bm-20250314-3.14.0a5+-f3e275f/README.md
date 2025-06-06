# Results

- fork: python/f3e275f1a92c0f668b13
- version: 3.14.0a5+
- config: 
- commit hash: [f3e275f](https://github.com/python/cpython/commit/f3e275f)
- commit date: 2025-03-14T07:04:40+08:00
- commit merge base: [1121c80fdad1fc1a175f4691f33272cf28a66e83](https://github.com/python/cpython/commit/1121c80fdad1fc1a175f4691f33272cf28a66e83)
- ref: f3e275f1a92c0f668b13

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13847208286)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250314-vultr-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f.json)

### vs. 3.12.6

- Geometric mean: 1.065x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250314-vultr-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-3.12.6.md)
- [📈time plot](bm-20250314-vultr-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.026x faster (HPT: reliability of 89.24%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250314-vultr-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250314-vultr-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-3.13.0rc2.svg)

