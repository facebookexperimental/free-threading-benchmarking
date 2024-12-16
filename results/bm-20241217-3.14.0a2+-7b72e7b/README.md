# Results

- fork: corona10/gh_115999_BINARY_SUB
- version: 3.14.0a2+
- config: 
- commit hash: [7b72e7b](https://github.com/corona10/cpython/commit/7b72e7b)
- commit date: 2024-12-17T00:45:30+09:00
- commit merge base: [70154855cf698560dd9a5e484a649839cd68dc7c](https://github.com/python/cpython/commit/70154855cf698560dd9a5e484a649839cd68dc7c)
- ref: gh_115999_BINARY_SUB

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12357231006)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-7b72e7b.json)

### vs. 3.12.6

- Geometric mean: 1.066x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-7b72e7b-vs-3.12.6.md)
- [📈time plot](bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-7b72e7b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.027x faster (HPT: reliability of 98.73%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-7b72e7b-vs-3.13.0rc2.md)
- [📈time plot](bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-7b72e7b-vs-3.13.0rc2.svg)

