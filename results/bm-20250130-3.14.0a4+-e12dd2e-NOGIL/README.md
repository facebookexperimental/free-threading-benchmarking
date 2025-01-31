# Results

- fork: nascheme/gh_129201_gc_mark_pr
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [e12dd2e](https://github.com/nascheme/cpython/commit/e12dd2e)
- commit date: 2025-01-30T20:43:15-08:00
- commit merge base: [4ca9fc08f89bf7172d41e523d9e520eb1729ee8c](https://github.com/python/cpython/commit/4ca9fc08f89bf7172d41e523d9e520eb1729ee8c)
- ref: gh_129201_gc_mark_pr

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13066803451)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4%2B-e12dd2e.json)

### vs. 3.12.6

- Geometric mean: 1.054x slower (HPT: reliability of 99.98%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4%2B-e12dd2e-vs-3.12.6.md)
- [📈time plot](bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4%2B-e12dd2e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.085x slower (HPT: reliability of 99.98%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4%2B-e12dd2e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4%2B-e12dd2e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.006x slower (HPT: reliability of 99.66%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4%2B-e12dd2e-vs-base-mem.svg)
- [📄table](bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4%2B-e12dd2e-vs-base.md)
- [📈time plot](bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4%2B-e12dd2e-vs-base.svg)

