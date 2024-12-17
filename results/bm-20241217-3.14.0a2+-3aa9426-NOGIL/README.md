# Results

- fork: corona10/gh_115999_BINARY_SUB
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [3aa9426](https://github.com/corona10/cpython/commit/3aa9426)
- commit date: 2024-12-17T10:58:01+09:00
- commit merge base: [70154855cf698560dd9a5e484a649839cd68dc7c](https://github.com/python/cpython/commit/70154855cf698560dd9a5e484a649839cd68dc7c)
- ref: gh_115999_BINARY_SUB

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12367415251)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426.json)

### vs. 3.12.6

- Geometric mean: 1.226x slower (HPT: reliability of 100.00%, 1.18x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426-vs-3.12.6.md)
- [📈time plot](bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.250x slower (HPT: reliability of 100.00%, 1.20x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426-vs-3.13.0rc2.md)
- [📈time plot](bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.006x faster (HPT: reliability of 99.92%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426-vs-base-mem.svg)
- [📄table](bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426-vs-base.md)
- [📈time plot](bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.267x slower (HPT: reliability of 100.00%, 1.27x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [📄table](bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426-vs-default_base_vs_NOGIL.svg)

