# Results

- fork: mpage/gh_115999_specialize
- version: 3.14.0a4+
- config: 
- commit hash: [3cedaed](https://github.com/mpage/cpython/commit/3cedaed)
- commit date: 2025-01-15T13:40:19-08:00
- commit merge base: [d05140f9f77d7dfc753dd1e5ac3a5962aaa03eff](https://github.com/python/cpython/commit/d05140f9f77d7dfc753dd1e5ac3a5962aaa03eff)
- ref: gh_115999_specialize

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12797514494)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed.json)

### vs. 3.12.6

- Geometric mean: 1.102x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-3.12.6.md)
- [📈time plot](bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.063x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-3.13.0rc2.md)
- [📈time plot](bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.016x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.02x
- [🧠memory plot](bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-base-mem.svg)
- [📄table](bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-base.md)
- [📈time plot](bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-base.svg)

