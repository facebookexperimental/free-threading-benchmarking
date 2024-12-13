# Results

- fork: python/487fdbed40734fd77214
- version: 3.14.0a2+
- config: 
- commit hash: [487fdbe](https://github.com/python/cpython/commit/487fdbe)
- commit date: 2024-12-12T11:22:20+00:00
- commit merge base: [292afd1d51dd7aacb12a6165f596ae7bb58c9ba8](https://github.com/python/cpython/commit/292afd1d51dd7aacb12a6165f596ae7bb58c9ba8)
- ref: 487fdbed40734fd77214

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12310924982)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2%2B-487fdbe.json)

### vs. 3.12.6

- Geometric mean: 1.085x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2%2B-487fdbe-vs-3.12.6.md)
- [📈time plot](bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2%2B-487fdbe-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.045x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2%2B-487fdbe-vs-3.13.0rc2.md)
- [📈time plot](bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2%2B-487fdbe-vs-3.13.0rc2.svg)

