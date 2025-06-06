# Results

- fork: python/7f882c88cfda48694797
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [7f882c8](https://github.com/python/cpython/commit/7f882c8)
- commit date: 2024-12-03T18:20:01-06:00
- commit merge base: [0f9107817022f0defac157e3795a4093a32ea320](https://github.com/python/cpython/commit/0f9107817022f0defac157e3795a4093a32ea320)
- ref: 7f882c88cfda48694797

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12150561963)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241203-vultr-x86_64-python-7f882c88cfda48694797-3.14.0a2%2B-7f882c8.json)

### vs. 3.12.6

- Geometric mean: 1.232x slower (HPT: reliability of 100.00%, 1.18x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241203-vultr-x86_64-python-7f882c88cfda48694797-3.14.0a2%2B-7f882c8-vs-3.12.6.md)
- [📈time plot](bm-20241203-vultr-x86_64-python-7f882c88cfda48694797-3.14.0a2%2B-7f882c8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.256x slower (HPT: reliability of 100.00%, 1.20x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241203-vultr-x86_64-python-7f882c88cfda48694797-3.14.0a2%2B-7f882c8-vs-3.13.0rc2.md)
- [📈time plot](bm-20241203-vultr-x86_64-python-7f882c88cfda48694797-3.14.0a2%2B-7f882c8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.268x slower (HPT: reliability of 100.00%, 1.27x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20241203-vultr-x86_64-python-7f882c88cfda48694797-3.14.0a2%2B-7f882c8-vs-base-mem.svg)
- [📄table](bm-20241203-vultr-x86_64-python-7f882c88cfda48694797-3.14.0a2%2B-7f882c8-vs-base.md)
- [📈time plot](bm-20241203-vultr-x86_64-python-7f882c88cfda48694797-3.14.0a2%2B-7f882c8-vs-base.svg)

