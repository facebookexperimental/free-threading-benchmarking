# Results

- fork: mpage/gh_115999_load_attr_
- version: 3.14.0a2+
- config: 
- commit hash: [0e874cd](https://github.com/mpage/cpython/commit/0e874cd)
- commit date: 2024-12-13T12:25:24-08:00
- commit merge base: [5dd775bed086909722ec7014a7c4f77a35f74a80](https://github.com/python/cpython/commit/5dd775bed086909722ec7014a7c4f77a35f74a80)
- ref: gh_115999_load_attr_

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12322649011)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-0e874cd.json)

### vs. 3.12.6

- Geometric mean: 1.088x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-0e874cd-vs-3.12.6.md)
- [📈time plot](bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-0e874cd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.048x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-0e874cd-vs-3.13.0rc2.md)
- [📈time plot](bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-0e874cd-vs-3.13.0rc2.svg)

