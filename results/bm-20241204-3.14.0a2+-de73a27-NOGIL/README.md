# Results

- fork: mpage/gh_115999_load_attr_
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [de73a27](https://github.com/mpage/cpython/commit/de73a27)
- commit date: 2024-12-04T16:34:18-08:00
- commit merge base: [51cfa569e379f84b3418db0971a71b1ef575a42b](https://github.com/python/cpython/commit/51cfa569e379f84b3418db0971a71b1ef575a42b)
- ref: gh_115999_load_attr_

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12189246879)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-de73a27.json)

### vs. 3.12.6

- Geometric mean: 1.219x slower (HPT: reliability of 100.00%, 1.16x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-de73a27-vs-3.12.6.md)
- [📈time plot](bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-de73a27-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.244x slower (HPT: reliability of 100.00%, 1.18x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-de73a27-vs-3.13.0rc2.md)
- [📈time plot](bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-de73a27-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.017x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-de73a27-vs-base-mem.svg)
- [📄table](bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-de73a27-vs-base.md)
- [📈time plot](bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-de73a27-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.263x slower (HPT: reliability of 100.00%, 1.25x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-de73a27-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-de73a27-vs-default_base_vs_NOGIL.svg)

