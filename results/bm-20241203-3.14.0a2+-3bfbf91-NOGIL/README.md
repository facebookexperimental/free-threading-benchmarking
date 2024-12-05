# Results

- fork: mpage/gh_115999_load_attr
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [3bfbf91](https://github.com/mpage/cpython/commit/3bfbf91)
- commit date: 2024-12-03T17:01:40-08:00
- commit merge base: [dabcecfd6dadb9430733105ba36925b290343d31](https://github.com/python/cpython/commit/dabcecfd6dadb9430733105ba36925b290343d31)
- ref: gh_115999_load_attr

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12150668256)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2%2B-3bfbf91.json)

### vs. 3.12.6

- Geometric mean: 1.219x slower (HPT: reliability of 100.00%, 1.18x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2%2B-3bfbf91-vs-3.12.6.md)
- [📈time plot](bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2%2B-3bfbf91-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.244x slower (HPT: reliability of 100.00%, 1.19x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2%2B-3bfbf91-vs-3.13.0rc2.md)
- [📈time plot](bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2%2B-3bfbf91-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.015x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2%2B-3bfbf91-vs-base-mem.svg)
- [📄table](bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2%2B-3bfbf91-vs-base.md)
- [📈time plot](bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2%2B-3bfbf91-vs-base.svg)

