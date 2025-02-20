# Results

- fork: DinoV/nolock_loadattr_with
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [6a1fe7e](https://github.com/DinoV/cpython/commit/6a1fe7e)
- commit date: 2025-02-19T11:10:54-08:00
- commit merge base: [ccf17323c218a2fdcf7f4845d3eaa74ebddefa44](https://github.com/python/cpython/commit/ccf17323c218a2fdcf7f4845d3eaa74ebddefa44)
- ref: nolock_loadattr_with

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13420492072)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5%2B-6a1fe7e.json)

### vs. 3.12.6

- Geometric mean: 1.038x slower (HPT: reliability of 99.95%, 1.02x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5%2B-6a1fe7e-vs-3.12.6.md)
- [📈time plot](bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5%2B-6a1fe7e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.070x slower (HPT: reliability of 99.98%, 1.04x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5%2B-6a1fe7e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5%2B-6a1fe7e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.006x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5%2B-6a1fe7e-vs-base-mem.svg)
- [📄table](bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5%2B-6a1fe7e-vs-base.md)
- [📈time plot](bm-20250219-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a5%2B-6a1fe7e-vs-base.svg)

