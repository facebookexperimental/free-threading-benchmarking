# Results

- fork: nascheme/gh_115999_load_super
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [ab3af14](https://github.com/nascheme/cpython/commit/ab3af14)
- commit date: 2024-11-26T11:44:04-08:00
- commit merge base: [09c240f20c47db126ad7e162df41e5c2596962d4](https://github.com/python/cpython/commit/09c240f20c47db126ad7e162df41e5c2596962d4)
- ref: gh_115999_load_super

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12039001236)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-ab3af14.json)

### vs. 3.12.6

- Geometric mean: 1.289x slower (HPT: reliability of 100.00%, 1.26x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-ab3af14-vs-3.12.6.md)
- [📈time plot](bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-ab3af14-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.313x slower (HPT: reliability of 100.00%, 1.29x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-ab3af14-vs-3.13.0rc2.md)
- [📈time plot](bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-ab3af14-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x faster (HPT: reliability of 99.76%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-ab3af14-vs-base-mem.svg)
- [📄table](bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-ab3af14-vs-base.md)
- [📈time plot](bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-ab3af14-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.306x slower (HPT: reliability of 100.00%, 1.29x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: html5lib
- [📄table](bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-ab3af14-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-ab3af14-vs-default_base_vs_NOGIL.svg)

