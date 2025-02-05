# Results

- fork: DinoV/noclock_clear
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [08975df](https://github.com/DinoV/cpython/commit/08975df)
- commit date: 2025-02-04T17:03:28-08:00
- commit merge base: [49f24650e4541456872490ec2b59d6d186204891](https://github.com/python/cpython/commit/49f24650e4541456872490ec2b59d6d186204891)
- ref: noclock_clear

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13164568577)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-08975df.json)

### vs. 3.12.6

- Geometric mean: 1.054x slower (HPT: reliability of 99.93%, 1.03x slower at 99th %ile)
- Memory usage: 1.46x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-08975df-vs-3.12.6.md)
- [📈time plot](bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-08975df-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.079x slower (HPT: reliability of 99.97%, 1.04x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-08975df-vs-3.13.0rc2.md)
- [📈time plot](bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-08975df-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.012x slower (HPT: reliability of 95.30%, 1.00x slower at 99th %ile)
- Memory usage: 1.10x
- [🧠memory plot](bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-08975df-vs-base-mem.svg)
- [📄table](bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-08975df-vs-base.md)
- [📈time plot](bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-08975df-vs-base.svg)

