# Results

- fork: mpage
- version: 3.14.0a2+
- config: 
- commit hash: [c0d3c19](https://github.com/mpage/cpython/commit/c0d3c19)
- commit date: 2024-12-04T11:06:24-08:00
- commit merge base: [51cfa569e379f84b3418db0971a71b1ef575a42b](https://github.com/mpage/cpython/commit/51cfa569e379f84b3418db0971a71b1ef575a42b)
- ref: gh_115999_tlbc_call_

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12166600558)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2%2B-c0d3c19.json)

### vs. 3.12.6

- Geometric mean: 1.057x faster (HPT: reliability of 99.83%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2%2B-c0d3c19-vs-3.12.6.md)
- [📈time plot](bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2%2B-c0d3c19-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.019x faster (HPT: reliability of 61.26%, 1.00x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2%2B-c0d3c19-vs-3.13.0rc2.md)
- [📈time plot](bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2%2B-c0d3c19-vs-3.13.0rc2.svg)

