# Results

- fork: colesbury/gh_129236_gc_stackpo
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [1ec055b](https://github.com/colesbury/cpython/commit/1ec055b)
- commit date: 2025-01-23T20:17:00+00:00
- commit merge base: [c05a851ac59e6fb7bd433677b9c116fb8336a8b1](https://github.com/python/cpython/commit/c05a851ac59e6fb7bd433677b9c116fb8336a8b1)
- ref: gh_129236_gc_stackpo

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12937349520)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4%2B-1ec055b.json)

### vs. 3.12.6

- Geometric mean: 1.048x slower (HPT: reliability of 99.98%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4%2B-1ec055b-vs-3.12.6.md)
- [📈time plot](bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4%2B-1ec055b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.078x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4%2B-1ec055b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4%2B-1ec055b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.010x faster (HPT: reliability of 87.63%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4%2B-1ec055b-vs-base-mem.svg)
- [📄table](bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4%2B-1ec055b-vs-base.md)
- [📈time plot](bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4%2B-1ec055b-vs-base.svg)

