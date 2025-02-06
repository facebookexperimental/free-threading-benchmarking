# Results

- fork: DinoV/noclock_clear
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [43173b7](https://github.com/DinoV/cpython/commit/43173b7)
- commit date: 2025-02-05T15:37:15-08:00
- commit merge base: [49f24650e4541456872490ec2b59d6d186204891](https://github.com/python/cpython/commit/49f24650e4541456872490ec2b59d6d186204891)
- ref: noclock_clear

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13168660166)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-43173b7.json)

### vs. 3.12.6

- Geometric mean: 1.042x slower (HPT: reliability of 99.97%, 1.02x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-43173b7-vs-3.12.6.md)
- [📈time plot](bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-43173b7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.073x slower (HPT: reliability of 99.98%, 1.04x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-43173b7-vs-3.13.0rc2.md)
- [📈time plot](bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-43173b7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x slower (HPT: reliability of 83.48%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-43173b7-vs-base-mem.svg)
- [📄table](bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-43173b7-vs-base.md)
- [📈time plot](bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-43173b7-vs-base.svg)

