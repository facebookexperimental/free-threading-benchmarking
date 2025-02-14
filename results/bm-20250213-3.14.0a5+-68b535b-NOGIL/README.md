# Results

- fork: DinoV/local_type_cache
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [68b535b](https://github.com/DinoV/cpython/commit/68b535b)
- commit date: 2025-02-13T15:44:48-08:00
- commit merge base: [05e89c34bd8389f87bd6c9462d5a06ef9e1a65ab](https://github.com/python/cpython/commit/05e89c34bd8389f87bd6c9462d5a06ef9e1a65ab)
- ref: local_type_cache

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13319304595)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-68b535b.json)

### vs. 3.12.6

- Geometric mean: 1.032x slower (HPT: reliability of 99.81%, 1.01x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-68b535b-vs-3.12.6.md)
- [📈time plot](bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-68b535b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.064x slower (HPT: reliability of 99.94%, 1.03x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-68b535b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-68b535b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.023x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-68b535b-vs-base-mem.svg)
- [📄table](bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-68b535b-vs-base.md)
- [📈time plot](bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-68b535b-vs-base.svg)

