# Results

- fork: mpage/gh_115999_load_attr_
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [3876bc7](https://github.com/mpage/cpython/commit/3876bc7)
- commit date: 2024-12-19T23:18:42-08:00
- commit merge base: [39e69a7cd54d44c9061db89bb15c460d30fba7a6](https://github.com/python/cpython/commit/39e69a7cd54d44c9061db89bb15c460d30fba7a6)
- ref: gh_115999_load_attr_

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12427270615)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-3876bc7.json)

### vs. 3.12.6

- Geometric mean: 1.091x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-3876bc7-vs-3.12.6.md)
- [📈time plot](bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-3876bc7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.120x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-3876bc7-vs-3.13.0rc2.md)
- [📈time plot](bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-3876bc7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.116x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.02x
- [🧠memory plot](bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-3876bc7-vs-base-mem.svg)
- [📄table](bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-3876bc7-vs-base.md)
- [📈time plot](bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-3876bc7-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.160x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-3876bc7-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-3876bc7-vs-default_base_vs_NOGIL.svg)

