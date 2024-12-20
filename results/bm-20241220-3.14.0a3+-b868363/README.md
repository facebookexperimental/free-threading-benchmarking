# Results

- fork: mpage/gh_115999_load_attr_
- version: 3.14.0a3+
- config: 
- commit hash: [b868363](https://github.com/mpage/cpython/commit/b868363)
- commit date: 2024-12-20T12:38:37-08:00
- commit merge base: [39e69a7cd54d44c9061db89bb15c460d30fba7a6](https://github.com/python/cpython/commit/39e69a7cd54d44c9061db89bb15c460d30fba7a6)
- ref: gh_115999_load_attr_

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12435974103)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-b868363.json)

### vs. 3.12.6

- Geometric mean: 1.094x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-b868363-vs-3.12.6.md)
- [📈time plot](bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-b868363-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-b868363-vs-3.13.0rc2.md)
- [📈time plot](bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-b868363-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.008x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-b868363-vs-base-mem.svg)
- [📄table](bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-b868363-vs-base.md)
- [📈time plot](bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-b868363-vs-base.svg)

