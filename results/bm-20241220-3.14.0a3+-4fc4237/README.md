# Results

- fork: mpage/4fc4237a1ea09f6a31e9
- version: 3.14.0a3+
- config: 
- commit hash: [4fc4237](https://github.com/mpage/cpython/commit/4fc4237)
- commit date: 2024-12-20T20:09:50-08:00
- commit merge base: [2a66dd33dfc0b845042da9bb54aaa4e890733f54](https://github.com/python/cpython/commit/2a66dd33dfc0b845042da9bb54aaa4e890733f54)
- ref: 4fc4237a1ea09f6a31e9

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12449614415)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241220-vultr-x86_64-mpage-4fc4237a1ea09f6a31e9-3.14.0a3%2B-4fc4237.json)

### vs. 3.12.6

- Geometric mean: 1.091x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241220-vultr-x86_64-mpage-4fc4237a1ea09f6a31e9-3.14.0a3%2B-4fc4237-vs-3.12.6.md)
- [📈time plot](bm-20241220-vultr-x86_64-mpage-4fc4237a1ea09f6a31e9-3.14.0a3%2B-4fc4237-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.052x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241220-vultr-x86_64-mpage-4fc4237a1ea09f6a31e9-3.14.0a3%2B-4fc4237-vs-3.13.0rc2.md)
- [📈time plot](bm-20241220-vultr-x86_64-mpage-4fc4237a1ea09f6a31e9-3.14.0a3%2B-4fc4237-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x faster (HPT: reliability of 99.25%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241220-vultr-x86_64-mpage-4fc4237a1ea09f6a31e9-3.14.0a3%2B-4fc4237-vs-base-mem.svg)
- [📄table](bm-20241220-vultr-x86_64-mpage-4fc4237a1ea09f6a31e9-3.14.0a3%2B-4fc4237-vs-base.md)
- [📈time plot](bm-20241220-vultr-x86_64-mpage-4fc4237a1ea09f6a31e9-3.14.0a3%2B-4fc4237-vs-base.svg)

