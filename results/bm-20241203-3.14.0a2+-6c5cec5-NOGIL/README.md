# Results

- fork: dpdani/gh_117657_tsan_pymem
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [6c5cec5](https://github.com/dpdani/cpython/commit/6c5cec5)
- commit date: 2024-12-03T01:17:21+00:00
- commit merge base: [bfb0788bfcaab7474c1be0605552744e15082ee9](https://github.com/python/cpython/commit/bfb0788bfcaab7474c1be0605552744e15082ee9)
- ref: gh_117657_tsan_pymem

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12131069383)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2%2B-6c5cec5.json)

### vs. 3.12.6

- Geometric mean: 1.253x slower (HPT: reliability of 100.00%, 1.21x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2%2B-6c5cec5-vs-3.12.6.md)
- [📈time plot](bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2%2B-6c5cec5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.278x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2%2B-6c5cec5-vs-3.13.0rc2.md)
- [📈time plot](bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2%2B-6c5cec5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.007x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2%2B-6c5cec5-vs-base-mem.svg)
- [📄table](bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2%2B-6c5cec5-vs-base.md)
- [📈time plot](bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2%2B-6c5cec5-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.290x slower (HPT: reliability of 100.00%, 1.30x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [📄table](bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2%2B-6c5cec5-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2%2B-6c5cec5-vs-default_base_vs_NOGIL.svg)

