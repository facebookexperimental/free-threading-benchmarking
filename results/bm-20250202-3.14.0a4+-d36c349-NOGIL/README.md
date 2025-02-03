# Results

- fork: corona10/gh_129533
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [d36c349](https://github.com/corona10/cpython/commit/d36c349)
- commit date: 2025-02-02T18:55:26+09:00
- commit merge base: [cf4c4ecc26c7e3b89f2e56893260a8a3319dab3d](https://github.com/python/cpython/commit/cf4c4ecc26c7e3b89f2e56893260a8a3319dab3d)
- ref: gh_129533

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13119124268)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250202-vultr-x86_64-corona10-gh_129533-3.14.0a4%2B-d36c349.json)

### vs. 3.12.6

- Geometric mean: 1.021x slower (HPT: reliability of 99.48%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250202-vultr-x86_64-corona10-gh_129533-3.14.0a4%2B-d36c349-vs-3.12.6.md)
- [📈time plot](bm-20250202-vultr-x86_64-corona10-gh_129533-3.14.0a4%2B-d36c349-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.053x slower (HPT: reliability of 99.87%, 1.02x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250202-vultr-x86_64-corona10-gh_129533-3.14.0a4%2B-d36c349-vs-3.13.0rc2.md)
- [📈time plot](bm-20250202-vultr-x86_64-corona10-gh_129533-3.14.0a4%2B-d36c349-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x faster (HPT: reliability of 99.87%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250202-vultr-x86_64-corona10-gh_129533-3.14.0a4%2B-d36c349-vs-base-mem.svg)
- [📄table](bm-20250202-vultr-x86_64-corona10-gh_129533-3.14.0a4%2B-d36c349-vs-base.md)
- [📈time plot](bm-20250202-vultr-x86_64-corona10-gh_129533-3.14.0a4%2B-d36c349-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.115x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- new benchmarks: html5lib
- [📄table](bm-20250202-vultr-x86_64-corona10-gh_129533-3.14.0a4%2B-d36c349-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250202-vultr-x86_64-corona10-gh_129533-3.14.0a4%2B-d36c349-vs-default_base_vs_NOGIL.svg)

