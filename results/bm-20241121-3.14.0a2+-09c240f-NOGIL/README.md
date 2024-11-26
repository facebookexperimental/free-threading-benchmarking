# Results

- fork: python
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [09c240f](https://github.com/python/cpython/commit/09c240f)
- commit date: 2024-11-21T11:22:21-08:00
- commit merge base: [9dabace39d118ec7a204b6970f8a3f475a11522c](https://github.com/python/cpython/commit/9dabace39d118ec7a204b6970f8a3f475a11522c)
- ref: 09c240f20c47db126ad7

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12020600304)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2%2B-09c240f.json)

### vs. 3.12.6

- Geometric mean: 1.292x slower (HPT: reliability of 100.00%, 1.26x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2%2B-09c240f-vs-3.12.6.md)
- [📈time plot](bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2%2B-09c240f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.316x slower (HPT: reliability of 100.00%, 1.29x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2%2B-09c240f-vs-3.13.0rc2.md)
- [📈time plot](bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2%2B-09c240f-vs-3.13.0rc2.svg)

