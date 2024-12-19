# Results

- fork: nascheme/gh_115999_specialize
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [9015a3f](https://github.com/nascheme/cpython/commit/9015a3f)
- commit date: 2024-12-18T10:37:05-08:00
- commit merge base: [329165639f9ac00ba64f6493dbcafcef6955e2cb](https://github.com/python/cpython/commit/329165639f9ac00ba64f6493dbcafcef6955e2cb)
- ref: gh_115999_specialize

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12399719461)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3%2B-9015a3f.json)

### vs. 3.12.6

- Geometric mean: 1.192x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3%2B-9015a3f-vs-3.12.6.md)
- [📈time plot](bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3%2B-9015a3f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.218x slower (HPT: reliability of 100.00%, 1.16x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3%2B-9015a3f-vs-3.13.0rc2.md)
- [📈time plot](bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3%2B-9015a3f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.023x faster (HPT: reliability of 99.99%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3%2B-9015a3f-vs-base-mem.svg)
- [📄table](bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3%2B-9015a3f-vs-base.md)
- [📈time plot](bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3%2B-9015a3f-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.247x slower (HPT: reliability of 100.00%, 1.24x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [📄table](bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3%2B-9015a3f-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3%2B-9015a3f-vs-default_base_vs_NOGIL.svg)

