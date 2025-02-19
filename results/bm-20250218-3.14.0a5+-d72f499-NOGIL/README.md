# Results

- fork: DinoV/local_type_cache
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [d72f499](https://github.com/DinoV/cpython/commit/d72f499)
- commit date: 2025-02-18T13:56:36-08:00
- commit merge base: [bcc9a5dddb777c8195b56645a15298cc0949ed9b](https://github.com/python/cpython/commit/bcc9a5dddb777c8195b56645a15298cc0949ed9b)
- ref: local_type_cache

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13400781040)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-d72f499.json)

### vs. 3.12.6

- Geometric mean: 1.055x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-d72f499-vs-3.12.6.md)
- [📈time plot](bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-d72f499-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.086x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-d72f499-vs-3.13.0rc2.md)
- [📈time plot](bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-d72f499-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.009x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-d72f499-vs-base-mem.svg)
- [📄table](bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-d72f499-vs-base.md)
- [📈time plot](bm-20250218-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-d72f499-vs-base.svg)

