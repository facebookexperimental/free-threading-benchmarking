# Results

- fork: mpage/gh_115999_specialize
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [3cedaed](https://github.com/mpage/cpython/commit/3cedaed)
- commit date: 2025-01-15T13:40:19-08:00
- commit merge base: [d05140f9f77d7dfc753dd1e5ac3a5962aaa03eff](https://github.com/python/cpython/commit/d05140f9f77d7dfc753dd1e5ac3a5962aaa03eff)
- ref: gh_115999_specialize

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12797511462)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed.json)

### vs. 3.12.6

- Geometric mean: 1.053x slower (HPT: reliability of 99.98%, 1.03x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-3.12.6.md)
- [📈time plot](bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.084x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-3.13.0rc2.md)
- [📈time plot](bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-3.13.0rc2.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.127x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-default_base_vs_NOGIL.svg)

