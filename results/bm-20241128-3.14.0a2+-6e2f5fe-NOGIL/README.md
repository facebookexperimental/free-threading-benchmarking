# Results

- fork: corona10/gh_115999_binary_sub
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [6e2f5fe](https://github.com/corona10/cpython/commit/6e2f5fe)
- commit date: 2024-11-28T00:42:38+09:00
- commit merge base: [58e334e1431b2ed6b70ee42501ea73e08084e769](https://github.com/python/cpython/commit/58e334e1431b2ed6b70ee42501ea73e08084e769)
- ref: gh_115999_binary_sub

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12059483461)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-6e2f5fe.json)

### vs. 3.12.6

- Geometric mean: 1.258x slower (HPT: reliability of 100.00%, 1.21x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-6e2f5fe-vs-3.12.6.md)
- [📈time plot](bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-6e2f5fe-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.283x slower (HPT: reliability of 100.00%, 1.24x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-6e2f5fe-vs-3.13.0rc2.md)
- [📈time plot](bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-6e2f5fe-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.007x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-6e2f5fe-vs-base-mem.svg)
- [📄table](bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-6e2f5fe-vs-base.md)
- [📈time plot](bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-6e2f5fe-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.274x slower (HPT: reliability of 100.00%, 1.24x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: html5lib
- [📄table](bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-6e2f5fe-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-6e2f5fe-vs-default_base_vs_NOGIL.svg)

