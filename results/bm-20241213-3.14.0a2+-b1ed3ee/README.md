# Results

- fork: mpage/gh_115999_load_attr_
- version: 3.14.0a2+
- config: 
- commit hash: [b1ed3ee](https://github.com/mpage/cpython/commit/b1ed3ee)
- commit date: 2024-12-13T21:07:57-08:00
- commit merge base: [5dd775bed086909722ec7014a7c4f77a35f74a80](https://github.com/python/cpython/commit/5dd775bed086909722ec7014a7c4f77a35f74a80)
- ref: gh_115999_load_attr_

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12327129636)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-b1ed3ee.json)

### vs. 3.12.6

- Geometric mean: 1.091x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-b1ed3ee-vs-3.12.6.md)
- [📈time plot](bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-b1ed3ee-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.053x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-b1ed3ee-vs-3.13.0rc2.md)
- [📈time plot](bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-b1ed3ee-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.007x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-b1ed3ee-vs-base-mem.svg)
- [📄table](bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-b1ed3ee-vs-base.md)
- [📈time plot](bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-b1ed3ee-vs-base.svg)

