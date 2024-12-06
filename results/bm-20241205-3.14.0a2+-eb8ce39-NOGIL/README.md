# Results

- fork: mpage/gh_115999_load_attr_
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [eb8ce39](https://github.com/mpage/cpython/commit/eb8ce39)
- commit date: 2024-12-05T22:01:50-08:00
- commit merge base: [e991ac8f2037d78140e417cc9a9486223eb3e786](https://github.com/python/cpython/commit/e991ac8f2037d78140e417cc9a9486223eb3e786)
- ref: gh_115999_load_attr_

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12193934508)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-eb8ce39.json)

### vs. 3.12.6

- Geometric mean: 1.212x slower (HPT: reliability of 100.00%, 1.16x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-eb8ce39-vs-3.12.6.md)
- [📈time plot](bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-eb8ce39-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.238x slower (HPT: reliability of 100.00%, 1.17x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-eb8ce39-vs-3.13.0rc2.md)
- [📈time plot](bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-eb8ce39-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.013x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-eb8ce39-vs-base-mem.svg)
- [📄table](bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-eb8ce39-vs-base.md)
- [📈time plot](bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-eb8ce39-vs-base.svg)

