# Results

- fork: mpage/revert_c3ae5c9
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [3edc57c](https://github.com/mpage/cpython/commit/3edc57c)
- commit date: 2025-02-01T14:32:34-08:00
- commit merge base: [cf4c4ecc26c7e3b89f2e56893260a8a3319dab3d](https://github.com/python/cpython/commit/cf4c4ecc26c7e3b89f2e56893260a8a3319dab3d)
- ref: revert_c3ae5c9

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13093073750)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4%2B-3edc57c.json)

### vs. 3.12.6

- Geometric mean: 1.051x slower (HPT: reliability of 99.97%, 1.03x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4%2B-3edc57c-vs-3.12.6.md)
- [📈time plot](bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4%2B-3edc57c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.082x slower (HPT: reliability of 99.98%, 1.04x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4%2B-3edc57c-vs-3.13.0rc2.md)
- [📈time plot](bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4%2B-3edc57c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.027x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4%2B-3edc57c-vs-base-mem.svg)
- [📄table](bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4%2B-3edc57c-vs-base.md)
- [📈time plot](bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4%2B-3edc57c-vs-base.svg)

