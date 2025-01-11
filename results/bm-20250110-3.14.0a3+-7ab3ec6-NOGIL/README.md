# Results

- fork: mpage/gh_115999_load_attr_
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [7ab3ec6](https://github.com/mpage/cpython/commit/7ab3ec6)
- commit date: 2025-01-10T13:07:57-08:00
- commit merge base: [1b39b502d33c68f52fd775c4e6c2174baddd40bd](https://github.com/python/cpython/commit/1b39b502d33c68f52fd775c4e6c2174baddd40bd)
- ref: gh_115999_load_attr_

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12717881644)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-7ab3ec6.json)

### vs. 3.12.6

- Geometric mean: 1.056x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-7ab3ec6-vs-3.12.6.md)
- [📈time plot](bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-7ab3ec6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.086x slower (HPT: reliability of 99.99%, 1.06x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-7ab3ec6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-7ab3ec6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.117x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-7ab3ec6-vs-base-mem.svg)
- [📄table](bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-7ab3ec6-vs-base.md)
- [📈time plot](bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-7ab3ec6-vs-base.svg)

