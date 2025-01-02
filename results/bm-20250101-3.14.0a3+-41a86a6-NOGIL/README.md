# Results

- fork: kumaraditya303/asyncio_tsafe
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [41a86a6](https://github.com/kumaraditya303/cpython/commit/41a86a6)
- commit date: 2025-01-01T12:40:22+00:00
- commit merge base: [bb9d955e16c5578bdbc72750fbbffc8313559109](https://github.com/python/cpython/commit/bb9d955e16c5578bdbc72750fbbffc8313559109)
- ref: asyncio_tsafe

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12584970160)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3%2B-41a86a6.json)

### vs. 3.12.6

- Geometric mean: 1.173x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3%2B-41a86a6-vs-3.12.6.md)
- [📈time plot](bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3%2B-41a86a6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.200x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3%2B-41a86a6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3%2B-41a86a6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.008x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3%2B-41a86a6-vs-base-mem.svg)
- [📄table](bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3%2B-41a86a6-vs-base.md)
- [📈time plot](bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3%2B-41a86a6-vs-base.svg)

