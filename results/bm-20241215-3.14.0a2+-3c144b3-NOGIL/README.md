# Results

- fork: mpage/gh_115999_for_iter_i
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [3c144b3](https://github.com/mpage/cpython/commit/3c144b3)
- commit date: 2024-12-15T12:05:40-08:00
- commit merge base: [2de048ce79e621f5ae0574095b9600fe8595f607](https://github.com/python/cpython/commit/2de048ce79e621f5ae0574095b9600fe8595f607)
- ref: gh_115999_for_iter_i

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12341882270)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3.json)

### vs. 3.12.6

- Geometric mean: 1.080x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-3.12.6.md)
- [📈time plot](bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.109x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-3.13.0rc2.md)
- [📈time plot](bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.164x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.02x
- [🧠memory plot](bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-base-mem.svg)
- [📄table](bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-base.md)
- [📈time plot](bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.151x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-default_base_vs_NOGIL.svg)

