# Results

- fork: DinoV/local_type_cache
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [32a747e](https://github.com/DinoV/cpython/commit/32a747e)
- commit date: 2025-02-19T16:20:16-08:00
- commit merge base: [73801864d866c76ae26a120b9db9de21b08f8b50](https://github.com/python/cpython/commit/73801864d866c76ae26a120b9db9de21b08f8b50)
- ref: local_type_cache

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13425031100)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-32a747e.json)

### vs. 3.12.6

- Geometric mean: 1.043x slower (HPT: reliability of 99.96%, 1.03x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-32a747e-vs-3.12.6.md)
- [📈time plot](bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-32a747e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x slower (HPT: reliability of 99.98%, 1.04x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-32a747e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-32a747e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x slower (HPT: reliability of 95.06%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-32a747e-vs-base-mem.svg)
- [📄table](bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-32a747e-vs-base.md)
- [📈time plot](bm-20250219-vultr-x86_64-DinoV-local_type_cache-3.14.0a5%2B-32a747e-vs-base.svg)

