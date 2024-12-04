# Results

- fork: mpage
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [4049072](https://github.com/mpage/cpython/commit/4049072)
- commit date: 2024-12-03T17:10:00-08:00
- commit merge base: [8ba9f5bca9c0ce6130e1f4ba761a68f74f8457d0](https://github.com/mpage/cpython/commit/8ba9f5bca9c0ce6130e1f4ba761a68f74f8457d0)
- ref: reapply_gc_changes

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12151068720)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2%2B-4049072.json)

### vs. 3.12.6

- Geometric mean: 1.255x slower (HPT: reliability of 100.00%, 1.21x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2%2B-4049072-vs-3.12.6.md)
- [📈time plot](bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2%2B-4049072-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.279x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2%2B-4049072-vs-3.13.0rc2.md)
- [📈time plot](bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2%2B-4049072-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x faster (HPT: reliability of 99.85%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2%2B-4049072-vs-base-mem.svg)
- [📄table](bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2%2B-4049072-vs-base.md)
- [📈time plot](bm-20241203-vultr-x86_64-mpage-reapply_gc_changes-3.14.0a2%2B-4049072-vs-base.svg)

