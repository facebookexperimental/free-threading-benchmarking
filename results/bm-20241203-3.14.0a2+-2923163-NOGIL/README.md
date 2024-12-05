# Results

- fork: mpage/revert_gc_changes
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [2923163](https://github.com/mpage/cpython/commit/2923163)
- commit date: 2024-12-03T09:27:31-08:00
- commit merge base: [8ba9f5bca9c0ce6130e1f4ba761a68f74f8457d0](https://github.com/python/cpython/commit/8ba9f5bca9c0ce6130e1f4ba761a68f74f8457d0)
- ref: revert_gc_changes

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12145110414)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2%2B-2923163.json)

### vs. 3.12.6

- Geometric mean: 1.255x slower (HPT: reliability of 100.00%, 1.21x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2%2B-2923163-vs-3.12.6.md)
- [📈time plot](bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2%2B-2923163-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.279x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2%2B-2923163-vs-3.13.0rc2.md)
- [📈time plot](bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2%2B-2923163-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x faster (HPT: reliability of 56.65%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2%2B-2923163-vs-base-mem.svg)
- [📄table](bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2%2B-2923163-vs-base.md)
- [📈time plot](bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2%2B-2923163-vs-base.svg)

