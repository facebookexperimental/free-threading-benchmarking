# Results

- fork: mpage/gh_115999_load_attr_
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [8b96368](https://github.com/mpage/cpython/commit/8b96368)
- commit date: 2025-01-02T11:28:47-08:00
- commit merge base: [8eebe4e6d02bb4ad3f1ca6c52624186903dce893](https://github.com/python/cpython/commit/8eebe4e6d02bb4ad3f1ca6c52624186903dce893)
- ref: gh_115999_load_attr_

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12590752512)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-8b96368.json)

### vs. 3.12.6

- Geometric mean: 1.060x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-8b96368-vs-3.12.6.md)
- [📈time plot](bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-8b96368-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.091x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-8b96368-vs-3.13.0rc2.md)
- [📈time plot](bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-8b96368-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.123x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.02x
- [🧠memory plot](bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-8b96368-vs-base-mem.svg)
- [📄table](bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-8b96368-vs-base.md)
- [📈time plot](bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-8b96368-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.142x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-8b96368-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-8b96368-vs-default_base_vs_NOGIL.svg)

