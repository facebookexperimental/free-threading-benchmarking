# Results

- fork: corona10/gh_115999_BINARY_SUB
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [47b80b4](https://github.com/corona10/cpython/commit/47b80b4)
- commit date: 2024-12-19T03:46:43+09:00
- commit merge base: [70154855cf698560dd9a5e484a649839cd68dc7c](https://github.com/python/cpython/commit/70154855cf698560dd9a5e484a649839cd68dc7c)
- ref: gh_115999_BINARY_SUB

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12399730578)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-47b80b4.json)

### vs. 3.12.6

- Geometric mean: 1.221x slower (HPT: reliability of 100.00%, 1.17x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-47b80b4-vs-3.12.6.md)
- [📈time plot](bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-47b80b4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.246x slower (HPT: reliability of 100.00%, 1.19x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-47b80b4-vs-3.13.0rc2.md)
- [📈time plot](bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-47b80b4-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.012x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-47b80b4-vs-base-mem.svg)
- [📄table](bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-47b80b4-vs-base.md)
- [📈time plot](bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-47b80b4-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.263x slower (HPT: reliability of 100.00%, 1.25x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [📄table](bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-47b80b4-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-47b80b4-vs-default_base_vs_NOGIL.svg)

