# Results

- fork: nascheme/gh_115999_specialize
- version: 3.14.0a3+
- config: 
- commit hash: [9015a3f](https://github.com/nascheme/cpython/commit/9015a3f)
- commit date: 2024-12-18T10:37:05-08:00
- commit merge base: [329165639f9ac00ba64f6493dbcafcef6955e2cb](https://github.com/python/cpython/commit/329165639f9ac00ba64f6493dbcafcef6955e2cb)
- ref: gh_115999_specialize

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12399722559)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3%2B-9015a3f.json)

### vs. 3.12.6

- Geometric mean: 1.082x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3%2B-9015a3f-vs-3.12.6.md)
- [📈time plot](bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3%2B-9015a3f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.043x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3%2B-9015a3f-vs-3.13.0rc2.md)
- [📈time plot](bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3%2B-9015a3f-vs-3.13.0rc2.svg)

