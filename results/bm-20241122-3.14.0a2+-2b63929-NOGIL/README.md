# Results

- fork: colesbury/gh_115999_store_subs
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [2b63929](https://github.com/colesbury/cpython/commit/2b63929)
- commit date: 2024-11-22T19:04:30+00:00
- commit merge base: [a264637654f9d3ac3c140e66fd56ee32faf22431](https://github.com/python/cpython/commit/a264637654f9d3ac3c140e66fd56ee32faf22431)
- ref: gh_115999_store_subs

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11978619636)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2%2B-2b63929.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.21x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2%2B-2b63929-vs-3.12.6.md)
- [📈time plot](bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2%2B-2b63929-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.25x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2%2B-2b63929-vs-3.13.0rc2.md)
- [📈time plot](bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2%2B-2b63929-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 99.99%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2%2B-2b63929-vs-base-mem.svg)
- [📄table](bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2%2B-2b63929-vs-base.md)
- [📈time plot](bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2%2B-2b63929-vs-base.svg)

