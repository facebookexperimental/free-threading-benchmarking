# Results

- fork: mpage/gh_115999_load_attr_
- version: 3.14.0a2+
- config: 
- commit hash: [39cab3f](https://github.com/mpage/cpython/commit/39cab3f)
- commit date: 2024-12-12T17:01:46-08:00
- commit merge base: [487fdbed40734fd7721457c6f6ffeca03da0b0e7](https://github.com/python/cpython/commit/487fdbed40734fd7721457c6f6ffeca03da0b0e7)
- ref: gh_115999_load_attr_

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12310924982)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-39cab3f.json)

### vs. 3.12.6

- Geometric mean: 1.080x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-39cab3f-vs-3.12.6.md)
- [📈time plot](bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-39cab3f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.041x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-39cab3f-vs-3.13.0rc2.md)
- [📈time plot](bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-39cab3f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x slower (HPT: reliability of 98.80%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-39cab3f-vs-base-mem.svg)
- [📄table](bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-39cab3f-vs-base.md)
- [📈time plot](bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-39cab3f-vs-base.svg)

