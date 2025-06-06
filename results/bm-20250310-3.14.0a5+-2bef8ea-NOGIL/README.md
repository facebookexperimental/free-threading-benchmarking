# Results

- fork: python/2bef8ea8ea045d20394f
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [2bef8ea](https://github.com/python/cpython/commit/2bef8ea)
- commit date: 2025-03-10T14:06:56+00:00
- commit merge base: [7cc99a54b755cc7cc0b3680fde7834cf612d4fbc](https://github.com/python/cpython/commit/7cc99a54b755cc7cc0b3680fde7834cf612d4fbc)
- ref: 2bef8ea8ea045d20394f

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13769442386)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250310-vultr-x86_64-python-2bef8ea8ea045d20394f-3.14.0a5%2B-2bef8ea.json)

### vs. 3.12.6

- Geometric mean: 1.042x slower (HPT: reliability of 99.99%, 1.02x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250310-vultr-x86_64-python-2bef8ea8ea045d20394f-3.14.0a5%2B-2bef8ea-vs-3.12.6.md)
- [📈time plot](bm-20250310-vultr-x86_64-python-2bef8ea8ea045d20394f-3.14.0a5%2B-2bef8ea-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250310-vultr-x86_64-python-2bef8ea8ea045d20394f-3.14.0a5%2B-2bef8ea-vs-3.13.0rc2.md)
- [📈time plot](bm-20250310-vultr-x86_64-python-2bef8ea8ea045d20394f-3.14.0a5%2B-2bef8ea-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.102x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250310-vultr-x86_64-python-2bef8ea8ea045d20394f-3.14.0a5%2B-2bef8ea-vs-base-mem.svg)
- [📄table](bm-20250310-vultr-x86_64-python-2bef8ea8ea045d20394f-3.14.0a5%2B-2bef8ea-vs-base.md)
- [📈time plot](bm-20250310-vultr-x86_64-python-2bef8ea8ea045d20394f-3.14.0a5%2B-2bef8ea-vs-base.svg)

