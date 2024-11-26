# Results

- fork: colesbury
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [a9e4872](https://github.com/colesbury/cpython/commit/a9e4872)
- commit date: 2024-11-22T14:20:17+00:00
- commit merge base: [29cbcbd73bbfd8c953c0b213fb33682c289934ff](https://github.com/colesbury/cpython/commit/29cbcbd73bbfd8c953c0b213fb33682c289934ff)
- ref: gh_127022_cheaper_st

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11974360678)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1%2B-a9e4872.json)

### vs. 3.12.6

- Geometric mean: 1.303x slower (HPT: reliability of 100.00%, 1.26x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1%2B-a9e4872-vs-3.12.6.md)
- [📈time plot](bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1%2B-a9e4872-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.327x slower (HPT: reliability of 100.00%, 1.29x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1%2B-a9e4872-vs-3.13.0rc2.md)
- [📈time plot](bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1%2B-a9e4872-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.026x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1%2B-a9e4872-vs-base-mem.svg)
- [📄table](bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1%2B-a9e4872-vs-base.md)
- [📈time plot](bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1%2B-a9e4872-vs-base.svg)

