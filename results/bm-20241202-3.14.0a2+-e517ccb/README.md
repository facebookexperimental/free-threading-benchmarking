# Results

- fork: nascheme/gh_115999_specialize
- version: 3.14.0a2+
- config: 
- commit hash: [e517ccb](https://github.com/nascheme/cpython/commit/e517ccb)
- commit date: 2024-12-02T11:34:10-08:00
- commit merge base: [15d6506d175780bb29e5fcde654e3860408aa93e](https://github.com/python/cpython/commit/15d6506d175780bb29e5fcde654e3860408aa93e)
- ref: gh_115999_specialize

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12129208802)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-e517ccb.json)

### vs. 3.12.6

- Geometric mean: 1.030x faster (HPT: reliability of 99.23%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-e517ccb-vs-3.12.6.md)
- [📈time plot](bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-e517ccb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.007x slower (HPT: reliability of 96.93%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-e517ccb-vs-3.13.0rc2.md)
- [📈time plot](bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-e517ccb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x slower (HPT: reliability of 55.67%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-e517ccb-vs-base-mem.svg)
- [📄table](bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-e517ccb-vs-base.md)
- [📈time plot](bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-e517ccb-vs-base.svg)

