# Results

- fork: nascheme/gh_115999_load_super
- version: 3.14.0a2+
- config: 
- commit hash: [a515a0d](https://github.com/nascheme/cpython/commit/a515a0d)
- commit date: 2024-11-25T11:22:18-08:00
- commit merge base: [09c240f20c47db126ad7e162df41e5c2596962d4](https://github.com/python/cpython/commit/09c240f20c47db126ad7e162df41e5c2596962d4)
- ref: gh_115999_load_super

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12021956687)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-a515a0d.json)

### vs. 3.12.6

- Geometric mean: 1.039x faster (HPT: reliability of 99.92%, 1.01x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-a515a0d-vs-3.12.6.md)
- [📈time plot](bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-a515a0d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.001x faster (HPT: reliability of 73.75%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-a515a0d-vs-3.13.0rc2.md)
- [📈time plot](bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-a515a0d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x faster (HPT: reliability of 70.21%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-a515a0d-vs-base-mem.svg)
- [📄table](bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-a515a0d-vs-base.md)
- [📈time plot](bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-a515a0d-vs-base.svg)

