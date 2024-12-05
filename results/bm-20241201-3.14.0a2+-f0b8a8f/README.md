# Results

- fork: corona10/gh_115999_binary_sub
- version: 3.14.0a2+
- config: 
- commit hash: [f0b8a8f](https://github.com/corona10/cpython/commit/f0b8a8f)
- commit date: 2024-12-01T16:09:12+09:00
- commit merge base: [58e334e1431b2ed6b70ee42501ea73e08084e769](https://github.com/python/cpython/commit/58e334e1431b2ed6b70ee42501ea73e08084e769)
- ref: gh_115999_binary_sub

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12101366956)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-f0b8a8f.json)

### vs. 3.12.6

- Geometric mean: 1.036x faster (HPT: reliability of 99.92%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-f0b8a8f-vs-3.12.6.md)
- [📈time plot](bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-f0b8a8f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.002x slower (HPT: reliability of 82.98%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-f0b8a8f-vs-3.13.0rc2.md)
- [📈time plot](bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-f0b8a8f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x faster (HPT: reliability of 83.78%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-f0b8a8f-vs-base-mem.svg)
- [📄table](bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-f0b8a8f-vs-base.md)
- [📈time plot](bm-20241201-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-f0b8a8f-vs-base.svg)

